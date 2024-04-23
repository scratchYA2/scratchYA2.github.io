<!--
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
        console.log(pyodide.runPython(`
          import os
          os.listdir()
        `));
      }
      main();
    </script>
  </body>
</html>
-->

<html>
  <head>
      <script src="https://cdn.jsdelivr.net/pyodide/v0.25.1/full/pyodide.js"></script>
  </head>
  <body>
    Pyodide test page <br>
    Open your browser console to see Pyodide output
    <script type="text/javascript">
      async function main(){
        let pyodide = await loadPyodide();
        console.log(pyodide.runPython(`
            import sys
            sys.version
        `));
        pyodide.runPython("print(1 + 2)");
      }
      main();
    </script>
  </body>
</html>
