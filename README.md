<html>
  <head>
    <script src="https://cdn.jsdelivr.net/pyodide/v0.25.1/full/pyodide.js"></script>
  </head>

  <body>
    <h2>Pyodide test page</h2>
    <p>Open your browser console to see Pyodide output</p>
    <script>
      async function main(){
        let pyodide = await loadPyodide();
        pyodide.runPython(`
          import os
          import js

          div = js.document.createElement("div")
          div.innerHTML = f'<h1>This element was created from Python</h1><p>{os.listdir()}</p>'
          js.document.body.prepend(div)

          with open('index.html', 'w') as f:
            f.write('Now the file has more content!')
        `);
      }
      main();
    </script>
  </body>
</html>
