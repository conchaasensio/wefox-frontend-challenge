# wefox front challenge

This project is a web app builded in **React** which must runs locally the given API using docker-compose and list, show, create, update and remove the resource comming from the Dockerized API.

## 🌐 Link to the App.

Should you like to take a look to the deployed app, [here you have the link](https://tbc).

> ℹ️ Please note that the first time you open the browser, it takes awhile to load.

---
## 🗂️ Content

1. [Project Structure](#-project-structure)
2. [Process](#️-process)
3. [How to run the App](#-how-to-run-the-app)
   1. [Pre-requeriments](#pre-requeriments)
   2. [Node](#️-node)
   3. [Docker](#-docker)
4. [Author](#-author)
***

## 🚀 How to run the App.

### Pre-requeriments

You need to have either [```Node```](https://nodejs.org/es/) or [```Docker```](https://www.docker.com/) previously installed in your computer.

To start using this project, clone this repo to a new directory.
> ```console
>  $ git clone https://github.com/conchaasensio/wefox-frontend-challenge.git
> ```

### ➡️ Node
***

You have to run npm install in order to install the necesary dependencies.
> ```console
> $ npm install
> ```

Once you have installed the dependencies, you are ready to run the app with ```npm start```. 
> ```console
> $ npm start
> ```

>  ```console
> $ cd client
> $ npm start
> ```

> 👉 Open http://localhost:3006 to view in the browser

Finally, to run the tests you need to introduce the following commands on your terminal:
```console
$ npm test
```

### 🐳 Docker
***

> ⚠️ Should you are a MacOS user, please note that this process might be a bit slow. Take it into account if you are using Docker on a MAC computer.

In case you are using Docker, first of all you need to write the following commands on your terminal:
> ```console
> $ docker-compose run server npm install
> $ docker-compose run client npm install
> ```

Once we have it installed, we introduce this command in our terminal to run the app:
> ```console
> $ docker-compose up
> ```

> 👉 Open http://localhost:3000 to view in the browser.

> Finally, to run the tests in client, you need to introduce the following commands on your terminal:
```console
$ docker-compose run client npm test
```

## 🧱 Project structure

```
/
|
|– client
|   |– src
|     |– components
|     |– services
|     |– stylesheets
|– server
```

> 👉 The project is divided into 2 parts: On the one hand, ```client```, which contains the React App. On the other hand, ```server```, which has the REST API coded in Node.js. 

## ⚒️ Process

### * Create a React Project

The first decision I hade to make was how to start a React project. Nowadays we have different options to do so: Create React App, Next.js, or configuring it using Vite or Webpack.

Although it is recommended to choose Next.js over Create React App (you can read more about ths¡is topic in this link), I finally decided to use Create React App because I have never worked wit Next.js before. Given the short deadeline to deliver the test, in practical terms, I decided to work with something that I had used before.

### * Run locally the API using docker-compose

It was the second time that I configured docker-compose by myself, but it was easy following the instructions given by wefox. I was provided with a pre-built image that includes the server API and the details of how to run the API server.

### ✳️ Using React Hooks

I have build this app using functional components from React. As you could see, I have used the hooks ```useState``` and ```useEffect```, linked to the component´s state and life cycle; as well as ```useParams``` and ```useNavigate``` linked to React Router.

### ✳️ React Router

This was one of the challenges that I had to face because, even though I have used React Router several times, it was the first time that I used the version 6, which is quite different.

You could see in [**App.tsx** file](src/App.tsx) that App component is contained within another component, named *BrowserRouter*. This is because I have used [**React Router**](https://reactrouter.com/) to specify the routes in the app using my React components.

Once the routes are declared, I can link the different components using both *Link* and *useNavigate*.

### ✳️ TypeScript

I was not used to working with TypeScript, so it has been quite challenging develop this app by facing the different and multiple error messages that emerged.

### ✳️ Material UI

Although I used SASS and BEM in previous projects, this time I decided to try to work with [**Material UI**](https://mui.com/) because I think it is really used in lot of projects and I wanted to test it. Furthermore, I assumed that it was going to help me so much with the UI and that I was going to be able to go faster. I am not completely sure about the latter, but at least I have learnt something new.

### ✳️ Showing a map

It had the chance to play with lat/long data in order to paint a map.

### ✳️ Testing with React Testing Library

I am really interested in all that having to do with clean code and best practices. Testing is something that I am starting to learn. Although I am not an "advanced user" regarding this practice, I wanted to try to put it into practice during this exercise. I have included [tests files](client/src/components/__tests__) for 2 of the components, using [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/).


## 👩‍💻 Author

This App has been developed by [**Concha Asensio**](https://github.com/conchaasensiomr).
