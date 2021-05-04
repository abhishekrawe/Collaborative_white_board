# Collaborative White Board:

- When you want to describes somethings to your friends or collegues or try to make diagram or structure understand using a diagram **_Collaborative white board_** is the best way to do so.

## Functionalities:

- Changing brush color.
- Changing brush size.
- Also allow multiple user to interact read & write along.

![Demo-Gif](preview/demo-video.gif)

## Working:

- In **Board.jsx** - When canvas data events will be received and the new image drawn on the canvas, the image will be constructed on the data, which is received from the server, so that the data basically is Base 64 encoded image string which is embedded from another user drawing that drawing is now be display on a screen i.e, display using canvas.

### Running on local Machine:

> Make sure you have the lastest version of NodeJS engine installed on your local Machine.

- Clone the repository to your local by pasting the below command in the terminal.

```bash
    git clone git@github.com:abhishekrawe/Collaborative_white_board.git
```

- Now, Open the folder in Visual Studio Code (or Text Editor). Then open the terminal and split that terminal into two parts as shown below:
![Terminal-Splitting](preview/terminal.gif)
- On 1st Terminal, Change the directory to **ui/whiteboard-collab**

```bash
    cd ui/whiteboard-collab
```

- Then install the required dependencies to run the ReactJS web-application using following commands.

```bash
    npm install
```

- Now, it's time to start the React web-app using the following commands.

```bash
    npm start
```

- If you face issue (pic2) then use the following commands

```bash
    npm install react-scripts --save
```

```bash
    node node_modules/react-scripts/scripts/start.js
```

- Or, if you have nodemon installed

```bash
    nodemon node_modules/react-scripts/scripts/start.js
```

- Last step to run the server. On 2nd Terminal, Change the directory to **server/** using the following commands

```bash
    cd server/
```

- Then run the server.js file using the following commands.

```bash
    node server.js
```

- Now, your local server is started and running on port 3000.

- Open the web-application from the two different browser which is like two different user you can see all activities done in one browser is reflecting to another browser.

## Exploring Codebase:

- We have two directories:
  - server/
  - ui/

#### Inside server we have

- **server.js** file that is using to run my code on server side inside 'ui' folder - We kept the react application we have two components in 'ui' folder

```
       ui -
        1.Container - (path\collaborative-whiteboard-master\ui\whiteboard-collab\src\components\container)
                Container.JSX
                Container.css
        we have .jsx file inside the individuals components folder
        2.board- (path\collaborative-whiteboard-master\ui\whiteboard-collab\src\components\board)
               Board.jsx
               Board.css
```

- Now if we open the **board.jsx** file, I have coded the drawing on canvas, we develop canvas in code in **board.jsx** file

- In **_container.jsx_** file we have the board components. We have server side NodeJS code were we develop socket.io connection for communication between two clients.

- If any user will draw something on board all the changes will be reflected to all connected user in real time. We are syncing canvas image data across all connected user using web socket protocol.

## TODO: Future commits

> I will be implementing the screen sharing idea with the help of javascript.
