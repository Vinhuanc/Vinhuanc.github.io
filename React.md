## React
- React is an efficient & flexible JavaScript library for building User Interfaces(UI). It lets developers build UI from isolated codes named "components".

- React has different components:
    - `React.Component` subclass:
        ``` JSX
            class ShoppingList extends React.Component {
                render() {
                    return (
                    <div className="shopping-list">
                        <h1>Shopping List for {this.props.name}</h1>
                        <ul>
                        <li>Instagram</li>
                        <li>WhatsApp</li>
                        <li>Oculus</li>
                        </ul>
                    </div>
                    ); 
                }
            }
            // Example usage: <ShoppingList name="Mark" />
        ```

- `props`: short for properties, the component's parameters
- `render`: returns hierarchy of view to display
- `state`: to remember things (ex: to remember a button got clicked). React components can have state by setting `this.state` in the constructor
``` JSX
    class Square extends React.Component {
        constructor(props) { // adds constructor to the class to initialize the state
        super(props); // in JS, always call "super" when defining constructors of a subclass. All React components that have a constructor should start with the "super(props)" call.
        this.state = { // initializes the state
        value: null,
        };
        }

        render() {
        return (
        <button className="square" onClick={() => this.setState({value: 'X'})}>
            {this.state.value}
        </button>
        );
        }
    }
```

