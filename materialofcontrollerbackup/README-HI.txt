CONTROLLER BACKUP — CLIENT EXE SETUP

Har client PC (PC-B, PC-C, PC-D...) par alag copy chalti hai. App selected folders mein supported document files dhoondhta hai, unki copies private Controller repo mein PC ke naam se upload karta hai, aur originals/filenames ko nahi badalta. Windows start par app background/tray mein chalta hai.

PEHLE: HAR PC KE LIYE EK UPLOAD TOKEN BANAYEIN
1. Main/admin PC A par apne GitHub account se sign in karein.
2. GitHub: Profile > Settings > Developer settings > Fine-grained tokens > Generate new token.
3. Resource owner UzumakIPaashu chunen, Repository access mein sirf Controller chunen.
4. Repository permissions mein Contents ko Read and write dein. Metadata read GitHub khud include karta hai.
5. PC-B ke liye alag token banayein, phir PC-C ke liye alag token. Har token sirf usi PC par enter karein. Token ko password ki tarah private rakhein.

CLIENT PC PAR
1. Git for Windows install karein; ismein Git Credential Manager chahiye. GitHub account browser login client PC par zaroori nahi.
2. ControllerBackup.exe chalayein. App current Windows user ke Programs folder mein install hokar setup kholega. Admin permission nahi chahiye.
3. Repo URL Controller ka pehle se set hai. GitHub username aur us PC ka fine-grained token paste karein.
4. PC ID set karein: pehla PC-B, doosra PC-C, aage PC-D...
5. Desktop, Documents, Downloads default selected hain. Jo folders nahi chahiye unhe remove karein; Add folder se specific jagah chun sakte hain.
6. Save and start dabayein. App token ko Windows Credential Manager mein save karta hai, settings file mein nahi.

USKE BAAD
- Client par baar-baar GitHub login/approval nahi maangega. Token expire/revoke hone par Settings mein naya token paste karna hoga.
- Folder changes par upload hota hai; safety ke liye har 2 minute mein rescan bhi hota hai.
- Internet na ho to local queue mein copies rakhta hai aur connection aane par retry karta hai.
- Repo mein backups/PC-B/Documents/... jaisa structure banta hai. Selected folder ka README marker add hota hai, isliye supported file na hone par bhi PC/folder GitHub par dikhega.
- A admin account se kisi PC ke browser mein private Controller repo kholkar files dekh/download kar sakta hai.
- Tray menu mein Sync now, Pause sync, Open local backup, Settings, Disable auto-start aur Exit hain.

SUPPORTED FILES
PDF, Word, Excel, PowerPoint, OpenDocument, CSV, TXT/Markdown, OneNote, Publisher aur Visio formats.
90 MB se badi single files upload nahi hoti.

IMPORTANT
- Controller repo PRIVATE rakhein. Token write access deta hai, isliye har PC ke liye unique token banayein.
- App sirf setup mein chune folders scan karta hai, poora PC nahi.
- Repo mein file delete karne se Git history ki purani copy automatically erase nahi hoti.
