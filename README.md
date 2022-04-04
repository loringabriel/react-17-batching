# Sample React 17 app

In React 17, state updates inside promises or setTimeouts will trigger a rerender for eact update.  [View React 18 example with automatic batching](https://github.com/loringabriel/react-18-automatic-batching)

```javascript
function App() {
  const [count, setCount] = useState(1);
  const [loading, setLoading] = useState(true);
  
  console.log("Rendered => Total Renders: ", renderCount);

  const handleOnClickAsync = () => {
    fetch("https://jsonplaceholder.typicode.com/todos/1").then(() => {
      setCount(count + 1);
      setLoading(false);
    });
  };
  return <button onClick={handleOnClickAsync}>Click me</button>
}
```

![CleanShot 2022-04-04 at 15 10 40](https://user-images.githubusercontent.com/28633412/161541785-6c32c806-3a10-42f2-a237-e05c361db3e1.gif)
