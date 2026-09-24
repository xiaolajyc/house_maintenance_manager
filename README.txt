# 房屋维护管理 PWA V44

本版本基于 V43，修复 Firebase Google 登录在 iPhone/Safari 上使用 signInWithPopup 时可能出现 “The requested action is invalid.” 的问题。

主要调整：
- Firebase Google 登录改为 signInWithRedirect，避免移动端 popup/认证窗口兼容问题
- 应用启动时处理 getRedirectResult
- 登录错误显示具体 Firebase error code，便于继续排查
- Service Worker cache 升级为 v44，避免旧版代码继续缓存
- 其余任务、历史、照片、Firestore、Storage、Google Drive 功能保持不变
