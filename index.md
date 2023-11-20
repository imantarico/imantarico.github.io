# Program Todo


> `Step-1` : Membuat Database `db_todo`

``
- Buat database dengan nama db_todo
- table users
  - id int(11) primary key auto_increment
  - username varchar(50)
  - password varchar(50)
- table tasks
```

> `Step-2` : Tambahkan file `login.php`
- masukkan perintah ini di dalam tag <body>
```
<div class="container min-vh-100 d-flex align-items-center justify-content-center">
        <form action="login.php" method="post" class="border rounded p-4">
            <div class="d-flex justify-content-center">
                <img src="img/logo.png" width="100px">
            </div>
            <div class="mb-3">
                <label for="username" class="form-label">Username</label>
                <input type="text" class="form-control" id="username" name="username" required>
            </div>
            <div class="mb-3">
                <label for="password" class="form-label">Password</label>
                <input type="password" class="form-control" id="password" name="password" required>
            </div>
            <button type="submit" name="submit" class="btn btn-primary">Login</button>
        </form>
    </div>
```


```php
<?php
    session_start();
    if (isset($_SESSION['status'])) {
        header("Location: index.php");
    }
    if (isset($_POST['submit'])) {
        include('koneksi.php');
        $query = "SELECT * FROM users WHERE username= '$_POST[username]' AND password= '$_POST[password]'";
        $result = mysqli_query($koneksi, $query);
        if ($result->num_rows > 0) {
            session_start();
            $_SESSION['username'] = $_POST['username'];
            $_SESSION['status'] = "login";
            header("Location: dashboard.php");
        } else {
            echo "<script>alert('Username atau Password salah!')</script>";
        }
    }
    ?>
```
