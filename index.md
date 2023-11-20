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
