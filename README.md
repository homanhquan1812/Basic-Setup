# NestJS
<div align="center">
  <img src="https://github.com/user-attachments/assets/1687c224-a79b-411c-82b4-abd25b2b1e1e" alt="NodeJS + ExpressJS Logo" width="600">
</div>

## Cách cài đặt
Mở Terminal lên, cài đặt **NestJS**:
```
npm i -g @nestjs/cli
```
sau đó tạo thư mục dự án, chạy:
```
nest new
```

Sau khi hoàn thành, dùng lệnh **npm run start** để mở website backend NestJS.

# ExpressJS
<div align="center">
  <img src="https://github.com/user-attachments/assets/d6f0107a-ea30-4d2b-95e3-3a011d592f46" alt="NodeJS + ExpressJS Logo" width="600">
</div>

## Cách cài đặt
### Bước 1
Mở Terminal lên, tạo dự án bằng cách chạy:
```
npm init
```
rồi hoàn thành quy trình cài đặt đầu tiên.

Sau đó, cài đặt những gói thư viện **All-in-one** này:

**1. MERN/PERN Stack**
```
npm install express nodemon morgan mongoose dotenv bcrypt express-session express-rate-limit fs jsonwebtoken cors connect-mongo connect-pg-simple mongoose-delete pg mysql2
```

**2. Handlebars/EJS**
```
npm install express nodemon morgan mongoose express-handlebars ejs express-ejs-layouts dotenv method-override bcrypt express-session express-rate-limit fs connect-mongo connect-pg-simple mongoose-delete jsonwebtoken pg mysql2
```

### Bước 2
Vào file <b>package.json</b>, thêm dòng này tại <b>scripts</b>:
```
"start": "nodemon src/index.js",
```
và chỉnh sửa dòng này ở trên:
```
"main": "src/index.js",
```
Gõ lệnh này để host backend:
```
npm start
```

Mở web `localhost:3000`. Đây là website mà ta sẽ xây dựng. Muốn ngưng host thì t nhấn `Ctrl + C`.


## Handlebars
<div align="center">
  <img src="https://github.com/user-attachments/assets/a91e185f-1b6a-48f6-bdc8-baa638873cb7" alt="NodeJS + ExpressJS Logo" width="600">
</div>

Ở đây, ta dùng định dạng `.hbs` cho các file Handlebars.

Ta cần hiểu cơ cấu project như sau:
```
Project
  |
  |__ config
	|__ db.js
  |__ node_modules
  |__ src
	|__ app
	      |__ controllers
		    |__ (Các file controller liên quan)
	      |__ models
		    |__ (Các file models liên quan)
	|__ public
	      |__ css
	      |__ img
	      |__ js
	|__ resources
	      |__ views
		    |__ layouts
			  |__ main.hbs
		    |__ partials
		    	  |__ footer.hbs
			  |__ header.hbs
		    |__ (Các page Handlebars)
	|__ routes
	      |__ index.js
	      |__ (Các file route liên quan)
	|__ util
	      |__ (Các file util liên quan)
	|__ index.js
  |__ .env
  |__ package-lock.json
  |__ package.json
```

Giải thích các thư mục, file:
* `config`: Chứa file kết nối database.
* `app`: 2 thư mục `models` và `controllers` lần lượt xử lý dữ liệu từ Database và vận hành các chức năng trên website.
* `public`: Chứa các thư mục `css`, `js`, `img`,...
* `resource/views`: Chứa các tập tin Handlebars.
* `routes`: Chứa file tạo đường link cho website.
* `util`: Chứa các tiện ích cho website.
* `.env`: Lưu String kết nối database, cổng PORT và các key API khác như SECRET_API, KEY_API,... 

## EJS
<div align="center">
  <img src="https://github.com/user-attachments/assets/9c4765d7-c528-4069-9b31-493c23006cd1" alt="NodeJS + ExpressJS Logo" width="600">
</div>

> Về cơ bản, phần Backend của **EJS** và **Handlebars** là như nhau.

Ở đây, ta dùng định dạng `.ejs` cho các file Handlebars.

Ta cần hiểu cơ cấu project như sau:
```
Project
  |
  |__ config
	|__ db.js
  |__ node_modules
  |__ src
	|__ app
	      |__ controllers
		    |__ (Các file controller liên quan)
	      |__ models
		    |__ (Các file models liên quan)
	|__ public
	      |__ css
	      |__ img
	      |__ js
	|__ views
	      |__ layouts
		    |__ main.ejs
	      |__ partials
		    |__ footer.ejs
		    |__ header.ejs
	      |__ (Các page EJS)
	|__ routes
	      |__ index.js
	      |__ (Các file route liên quan)
	|__ util
	      |__ (Các file util liên quan)
	|__ index.js
  |__ .env
  |__ package-lock.json
  |__ package.json
```

# ReactJS

<div align="center">
  <img src="https://github.com/user-attachments/assets/f8e7f629-912e-4917-92e0-2536e2434014" alt="NodeJS + ExpressJS Logo" width="600">
</div>

## Bước 1
Tạo project ReactJS bằng **Vite**, phiên bản này tối ưu hơn ReactJS truyển thống:
```
npm create vite@latest
```

Chọn **React** rồi **Javascript**, sau đó hoàn thành quy trình cài đặt. Tiếp theo, làm theo hướng dẫn trên terminal.

**http://localhost:5173** là website ReactJS của bạn.

## Bước 2
Cài đặt những gói thư viện cần thiết này:
```
npm install react-router-dom react-helmet axios jwt-decode vite-plugin-mkcert jquery
```

Cụ thể hơn:
* `react-router-dom`: Dùng để quản lý điều hướng trong website.
* `react-helmet`: Dùng để quản lý các tài nguyên trong `<head>` hoặc **script** trong `<body>`,...
* `jwt-decode`: Giải mã token của JWT.
* `vite-plugin-mkcert`: Dùng `https` thay vì `http` cho web ReactJS.
* `jquery`: Thư viện jQuery.
**Chú ý**: Trong các dự án lớn, đừng nhét các file `css` và `js` vào **Helmet**, sẽ gây lỗi load file CSS và JS chậm.

và cài thêm <b>ES7+ React/Redux/React-Native snippets</b>.

ReactJS sẽ mặc định dùng `http`, nếu muốn dùng `https` thì chỉnh file `vite.config.js`:
```
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import mkcert from 'vite-plugin-mkcert'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [ mkcert(), react() ]
})
```

## Bước 3
Mở file `main.jsx` trong mục `src`, chép đoạn code sau:
```
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'
import { BrowserRouter } from 'react-router-dom'
import './../public/css/index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <BrowserRouter>
    <App />
  </BrowserRouter>
)
```

Tại `App.jsx`, đây là page chính chứa các **routes** để nối các page khác của web

## Bước 4
Ta cần hiểu cơ cấu project như sau:
```
Project
  |__ public
  	|__ css
	|__ img
	|__ js
  |__ src
	|__ components
	|__ pages
	|__ App.jsx
	|__ main.jsx
  |__ (Các file liên quan khác)
```

Tạo 2 thư mục `pages` và `components` lần lượt chứa page ReactJS và các thành phần khác như `head`,...; sau đó page bằng cách gõ `rafce` rồi nhét vào thư mục `pages`.

Trong folder `src`, ta sẽ tạo 2 file: **SampleReactJSPage.jsx** và **Home**. Ta xóa code ở **App.jsx** và chép đoạn code này cho **SampleReactJSPage.jsx**:
```
import { useState } from 'react'
import reactLogo from './../assets/react.svg'
import viteLogo from '/vite.svg'
import './../../public/css/App.css'

function SampleReactJSPage() {
  const [count, setCount] = useState(0)

  return (
    <>
      <div>
        <a href="https://vitejs.dev" target="_blank">
          <img src={viteLogo} className="logo" alt="Vite logo" />
        </a>
        <a href="https://react.dev" target="_blank">
          <img src={reactLogo} className="logo react" alt="React logo" />
        </a>
      </div>
      <h1>Vite + React</h1>
      <div className="card">
        <button onClick={() => setCount((count) => count + 1)}>
          count is {count}
        </button>
        <p>
          Edit <code>src/App.jsx</code> and save to test HMR
        </p>
      </div>
      <p className="read-the-docs">
        Click on the Vite and React logos to learn more
      </p>
    </>
  )
}

export default SampleReactJSPage
```

Trong **App.jsx**, ta chép đoạn code sau:
```
import React from 'react'
import { Routes, Route } from 'react-router-dom'
import Error from './pages/Error'
import Home from './pages/Home'
import SampleReactJSPage from './pages/SampleReactJSPage'

const App = () => {
  return (
    <Routes>
      <Route path="/" element={<Home></Home>}></Route>
      <Route path="/home" element={<Home></Home>}></Route>
      <Route path="/sample" element={<SampleReactJSPage></SampleReactJSPage>}></Route>
      <Route path="*" element={<Error></Error>}></Route>
    </Routes>
  )
}

export default App
```

Thế là ta đã xong 1 website có 2 trang chính và 1 trang phụ.

# React Native
<div align="center">
  <img src="https://github.com/user-attachments/assets/7d2edc86-4457-4381-a988-7aa6bd3f302e" alt="NodeJS + ExpressJS Logo" width="600">
</div>

1. Mở Terminal, gõ:
```
npx create-expo-app@latest
``` 

# Deploy Full-stack project lên Render
<div align="center">
  <img src="https://github.com/user-attachments/assets/8e3bacf0-91a0-4994-a9ad-b45430b2fccb" alt="NodeJS + ExpressJS Logo" width="600">
</div>

## MERN/PERN Stack
> Thư mục project phải có đủ 2 thư mục **backend** và **frontend**.
### Deploy Backend
1. Chọn **Web Service**.
2. Trong phần **Root Directory**, gõ `backend`.
3. Trong phần **Build Command**, gõ `npm install`.
4. Trong phần **Start Command**, gõ `node src/index.js`.
5. Thêm **.env** vào.

> Ưu điểm: Setup dễ.

> Nhược điểm: Chậm.
   
### Deploy Frontend
1. Chọn **Static Site**.
2. Chỉnh **CORS**, các link API trong **backend** sao cho phù hợp với link API đã deploy.
3. Trong phần **Root Directory**, gõ `frontend`.
4. Trong phần **Build Command**, gõ `npm install; npm run build`.
5. Trong phần **Publish directory**, gõ `dist`.
6. Thêm **.env** vào.
7. Vào phần **Redirects/Rewrites**, làm theo như sau:
   ![image](https://github.com/user-attachments/assets/14d0caee-a736-463c-a849-7916ad524d26)

## Handlebars/EJS
(Như deploy Backend ở trên)

# Deploy Backend lên Vercel
<div align="center">
  <img src="https://github.com/user-attachments/assets/2053d549-8132-41de-a83b-098463900852" alt="NodeJS + ExpressJS Logo" width="600">
</div>

1. Tạo file **vercel.json** trong thư mục **Backend**.

```
{
    "version": 2,
    "builds": [
        {
            "src": "src/index.js",
            "use": "@vercel/node"
        }
    ],
    "routes": [
        {
            "src": "/(.*)",
            "dest": "src/index.js"
        }
    ]
}
```

2. Deploy trên web **Vercel**.
3. Cài **Vercel** trên máy tính. Dùng lệnh này trên **Terminal**:
   
```
vercel --prod
```

> Ưu điểm: Nhanh.

> Nhược điểm: Setup khó và phải deploy lại khi project có update trên Github (Dù không liên quan tới Backend).


# Kiến thức cơ bản khác trong Backend
## Các status cơ bản từ các lệnh thực thi **CRUD** trên dữ liệu JSON
<div align="center">
  <img src="https://github.com/user-attachments/assets/d7acc486-93da-433a-b647-24eafae76aca" width="600">
</div>

* `200`: Lấy, cập nhật, xóa dữ liệu thành công.
* `201`: Tạo dữ liệu thành công.
* `400`: Thiếu thông tin cần thiết.
* `401`: Lỗi xác thực (Login, Register,...).
* `404`: Không tìm thấy dữ liệu.
* `409`: Trùng lặp thông tin.
* `500`: Lỗi server (Thường xảy ra ở Backend như code không phù hợp,...).

## Chi tiết các thư viện của NodeJS

<div align="center">
  <img src="https://github.com/user-attachments/assets/0da0bd7f-e8b2-4f0a-8f01-b2869e572ca8" alt="NodeJS + ExpressJS Logo" width="600">
</div>

* `express`: Chứa các tập tin cần thiết của NodeJS và ExpressJS để xây dựng Backend.
```
npm install express
```
* `nodemon`: Giúp khởi động lại ứng dụng Node khi phát hiện có sự thay đổi file hoặc code trong file của dự án.
```
npm install nodemon
```
* `morgan`: Cho phép ta dễ dàng ghi lại các yêu cầu, lỗi và hơn thế nữa vào **Console/Terminal**. Thường được sử dụng để coi web hỗ trợ Real-time Data (cập nhật thông tin ngay lập tức) hay không.
```
npm install morgan
```
* `mongoose`: Là một thư viện mô hình hóa đối tượng (Object Data Model - ODM) cho MongoDB và Node.js, được dùng để quản lý các kiểu dữ liệu từ database để website có thể sử dụng.
```
npm install mongoose
```
* `express-handlebars`: Chứa các tập tin cần thiết của Handlebars để thay thế cho HTML thông thường.
```
npm install express-handlebars
```
* `dotenv`: Giúp lưu trữ các thông tin nhạy cảm như **API KEY** hoặc **SECRET KEY** bên ngoài mã nguồn, giảm nguy cơ lộ thông tin khi chia sẻ mã nguồn.
```
npm install dotenv
```
* `bcrypt`: Tăng bảo mật cho Login/Register.
```
npm install bcrypt
```
* `method-override`: Dùng để cập nhật/xóa dữ liệu (Chỉ dùng cho Handlebars/EJS).
```
npm install method-override
```
* `cors`: à một cơ chế cho phép nhiều tài nguyên khác nhau của một trang web có thể được truy vấn từ domain khác với domain của trang đó.
```
npm install cors
```
* `pg`: Chứa các dữ liệu cần thiết để kết nối database PostgreSQL.
```
npm install pg
```
* `mysql2`: Chứa các dữ liệu cần thiết để kết nối database MySQL (Bản `mysql2` tốt hơn `mysql`).
```
npm install mysql2
```
* `ejs`: Chứa các tập tin cần thiết của EJS để thay thế cho HTML thông thường.
```
npm install ejs
```
* `express-ejs-layouts`: Không giống như **Handlebars**, ta phải cài thêm **layouts** để chứa các file page.
```
npm install express-ejs-layouts
```
* `express-session`: Session & Cookie
  - **Session**: Là phiên làm việc giữa client và server, thông tin phiên làm việc được lưu trữ trên server và được liên kết với 1 session ID duy nhất. Session sẽ kết thúc khi bạn tắt trình duyệt. **Cơ cấu hoạt động:** Sau khi đăng nhập xong (mình sẽ tạm gọi đây là request đầu tiên), server sẽ tạo một session và dữ liệu của session sẽ được lưu ở trên bộ nhớ của server. Mỗi session thì có một ID riêng, và ID này sẽ được lưu ở cookie trên trình duyệt của người dùng. Từ request thứ 2 trở đi, cookie sẽ được gửi kèm theo mỗi request. Server có thể so khớp session ID trong cookies được gửi kèm kia với session data lưu ở trong bộ nhớ, qua đó xác thực danh tính của người dùng vào trả về response. Đến khi đăng xuất, toàn bộ session data này sẽ bị xóa khỏi bộ nhớ.

  - **Cookie**: Là đoạn dữ liệu được lưu trữ trong trình duyệt, thường được sử dụng để lưu trữ session ID, sở thích của người dùng trên Internet,...
```
npm install express-session
```
* `express-rate-limit`: Giới hạn số lần đăng nhập sai.
```
npm install express-rate-limit
```
* `jsonwebtoken`: JWT là một tiêu chuẩn mở cho việc tạo ra các token truy cập an toàn dựa trên JSON, thường được sử dụng để xác thực và ủy quyền người dùng trong ứng dụng web và di động.

Thông thường, nếu so với `Session`:
   * `Session`: Bảo mật tốt hơn. Nhược điểm là nếu hoạt động nhiều server cùng 1 lúc, session ID gửi kèm theo request thì có thể được tìm thấy ở server này nhưng lại không ở server khác, dẫn đến trải nghiệm tồi tệ.
   * `JWT`: Hiệu suất và khả năng mở rộng tốt hơn vì token được lưu ở phía **Client**, không phải ở phía **Server** như `Session` nên tối ưu bộ nhớ hơn. Nhược điểm là: JWT chứa thông tin người dùng nhiều hơn so với Session ID và phải cẩn thận về vấn đề bảo mật hơn như lưu trữ token,...
```
npm install jsonwebtoken
```
* `mongoose-delete` (Tùy chọn - Chỉ dành cho MongoDB): Thay vì xóa hẳn dữ liệu khỏi database, ta dùng thư viện để **xóa mềm** bằng cách đặt `deleted: true` hoặc `deleted: false`.
```
npm install mongoose-delete
```
