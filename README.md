# 01 Starter

## Babel / Styling / Boolean

```javascript
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
<script crossorigin src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/6.26.0/babel.min.js"></script>
<link rel="stylesheet" href="app.css" />
<title>React Dev</title>
</head>

<body>

  <h1>React</h1>
  <div id="root">Wating</div>

  <script type="text/babel">
    const title = "My title";
    const style = {
      color: "teal"
    }
    const styleFalse = {
      color: "red"
    }
    
    let styleSelecter = function(msg, color, weight){
      const colors = {
        color: color,
        fontWeight: weight
      }
      return <span style={colors}>{msg}</span>
    }
    
    let setColor = function(msg, size, color){
      const fontStyle = {
        fontSize: size + "px",
        color: color,
      };
      return <p style={fontStyle}>{msg}</p>
    }
    
    let flg = false;
    
    let dom = document.querySelector('#root');
    let el = (
      <div>
        {flg ? <p>{styleSelecter("true", "pink", 800)}</p> : <p>{styleSelecter("false", "red", 800)}</p>}
        
        <h2 style={style}>{title}</h2>
        <p>{setColor("Hello", 24, "orange")}</p>
        <p>{setColor("MyWorld", 32, "navy")}</p>
      </div>
    );
    ReactDOM.render(el, dom);
  </script>

</body>
</html>
```

