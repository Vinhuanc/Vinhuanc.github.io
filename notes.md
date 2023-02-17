### React Notes
- when data changes, React will update and rerender components automatically
- to allow child components to communicate with each other, declare a share state
    in the parent component. The parent component can pass down the state to the children
    by props. This keeps all child components synced with parent components.

- two approaches to changing data: 
    1) Mutate the data by directly changing the data's values
        ``` JSX
            var player = { score: 1, name: "Jeff"};
            player.score = 2;
            // player's is now: score:2, name:"Jeff"
        ```
    2) Replace data with new copy which has the desired changes
        ```  JSX
            var player = { score: 1, name: "Jeff"};
            var newPlayer = Object.assign({}, player, {score: 2});
            // player remains unchanged
            // newPlayer is now: {score: 2, name:"Jeff"}

            // the object spread syntax way
            var newPlayer = {...player, score : 2};
        ```


