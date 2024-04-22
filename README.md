# PHP_Password_Encryption

<?php ?>
<head>
    <link rel="stylesheet" href="style.css">
</head>
<body>


    <form action="home.php" method="post">

        <input type="text" name="username" placeholder="username">
        <input type="email" name="email" placeholder="email">
        <input type="password" name="password" placeholder="password">
        <input type="submit" value="submit">
    
    
    </form>



    
</body>

//.................................................................
//..................................................................
<body style="background-color: lightblue;text-align: center;">


<?php

    $usrName = $_REQUEST['username'];
    $usrEmail = $_REQUEST['email'];
    $usrPass = $_REQUEST['password'];

    echo $usrPass;
    echo "<br>";

    $hash_format = "$2y$08$";
    
    $salt = "meuttheardiraavgtasdrk";
    $conC = $hash_format . $salt;

    echo crypt($usrPass,$conC);
?>

    
</body>






