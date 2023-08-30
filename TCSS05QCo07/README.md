## Tailwind CSS 05
## Chapter 5: Theme Config & Deploy to the Web
It is my coding practice with the TUTORIAL of Dave Gray. 

## Source
### Dave Gray 的 Tailwind CSS 資源
https://github.com/gitdagray/tailwind-css-course

### Dave Gray 的 Tailwind CSS 課程
https://youtube.com/playlist?list=PL0Zuz27SZ-6M8znNpim8dRiICRrP5HPft&si=TYz4MlVwoMJZuO69

### Dave Gray 的 YouTube 頻道
https://www.youtube.com/@DaveGrayTeachesCode

## Quick Concept offline
###  1. Intro
        教學影片開頭和介紹

###  2. Welcome

###  3. Starter Code
        (1)在 terminal 輸入 npx tailwindcss init
        (2)新增資料夾 build
        (3)新增資料夾 src
        (4)新增 input.css
        (5)新增 base
        (6)新增 components
        (7)新增 utilities
        (8)新增 index.html，修改 index.html
        (9)新增資料夾 img
        (10)新增 rocketride.png, rocketman.png, rocketlaunch.png, rocketdab.png
        (11)新增 favicon.ico
        (12)新增資料夾 js
        (13)新增 main.js
        (14)加入 html 路徑為 ./build/*.html
        加入 javascript 路徑為 ./build/js/*.js
        (15)在 terminal 輸入 npm init -y
        (16)在 package.json 的 scripts，
        設定 tailwind，指令為 npx tailwindcss -i ./src/input.css -o ./build/css/style.css --watch
        (17)在 terminal 輸入 npm i -D prettier-plugin-tailwindcss
        (18)新增 .gitignore，輸入 node_modules
        (19)在 package.json 的 scripts，
        設定 prettier，指令為 npx prettier --write **/*.html

###  4. Start tailwindcss
        在 terminal 輸入 npm run tailwind
        即在 terminal 執行 npx tailwindcss -i ./src/input.css -o ./build/css/style.css --watch

###  5. Media Query Adjustment
        tailwind.config.js
        在 extend 中，修改 tallscreen 為最大長寬比例
        輸入 screens: {
                "widescreen": { "raw": "(min-aspect-ratio: 3/2)"},
                "tallscreen": { "raw": "(max-aspect-ratio: 13/20)"},
        }

###  6. Content File Paths
        可以修改 html 和 javascript 路徑為 ./build/
        **/*.{html,js}

###  7. Extending Your Theme
        (1)在 extend 中，新增 colors 顏色為 papayawhip
        輸入 colors: {
                papayawhip: {
                        light: "#fef4e4",
                        DEFAULT: "#ffefd5",
                        dark: "#fee5bc"
                }
        }
        (2)如果僅需要新增顏色一次，可以輸入 text-[#ffefd5]

###  8. Send Project to Github
        (1)Git
        https://git-scm.com/
        (2)GitHub
        https://github.com/
        (3)點擊 New，
        輸入 Repository name
        Create a new repository，
        點擊 Create repository
        (4)在 terminal 輸入 git init
        (5)在 terminal 輸入 git add .
        (6)在 terminal 輸入 git commit -m "first commit"
        (7)在 terminal 輸入 git remote add origin 網址連結
        在 terminal 輸入 git branch -M main
        在 terminal 輸入 git push -u origin main

###  9. Deploy to Render.com
        (1)Render
        https://render.com/
        (2)點擊 New
        (3)點擊 Connect account
        (4)點擊 Connect
        (5)輸入 Name 進行命名
        (6)在 Publish directory 輸入 build
        (7)點擊 Create Static Site

        新增 favicon
        (8)移動 favicon.ico 至 build 資料夾
        (9)在 terminal 輸入 git status
        (10)在 terminal 輸入 git add .
        (11)在 terminal 輸入 git commit -m "Moved favicon to build directory"
        (12)在 terminal 輸入 git push

### 10. Next Steps
        使用 tailwind 修改 The Little Taco Shop
