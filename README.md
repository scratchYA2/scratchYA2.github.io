<html>
  <head>
    <script defer src="https://cdn.jsdelivr.net/pyodide/v0.25.1/full/pyodide.js">
  </head>

  <body>
    <h2>Pyodide test page</h2>
    <p>Open your browser console to see Pyodide output</p>
    <script>
      async function main(){
        let pyodide = await loadPyodide();
        console.log(pyodide.runPython(`
          import os
          os.listdir()
        `));
      }
      main();
    </script>
  </body>
</html>
