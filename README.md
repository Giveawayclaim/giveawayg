<html>
  <head>
   <title>moralis</title>
   <script src="https://cdn.jsdelivr.net/npm/web3@latest/dist/web3.min.js"></script>
   <script src="https://unpkg.com/moralis/dist/moralis.js"></script>
 </head>

  <body>
   <h1>Moralis Login</h1>

   <button onclick="login()" id="login">login</button>

   <script>
     const serverUrl = "https://eof90ibsnqds.usemoralis.com:2053/server";
     const appId = "L0FgRpI7Rp2unieOqCK5WLjXw70Wg8SZLz7ntTzu";
     Moralis.start({ serverUrl, appId });

     async function login() {
       const user = await Moralis.authenticate()
       document.getElementById("login").innerHTML = user.get("ethAddress")
     }
    </script>
   </body>


</html>
