# AmeliaLunggita_Modul7_bg1_bg2

1. Berikan contoh kode keneksi untuk ke database pd php?

    $host = "localhost";
    $db = "db_universitas";
    $uname = "root";
    $pass = "";

   $connect = mysqli_connect($host, $uname, $pass, $db);
    
2. Bagaimana cara anda membuat database pada phpMySQl!

ketik localhost/phpmyadmin/ kotak pencarian
lalu klik menu database dan klik new
lalu akan ditampilkan create database. edit nama database lalu klik create. maka database berhasil dibuat

3. Berikan code query untuk menampilkan sebuah data yang ada pada ke database?


include '../connect.php';

$id_dosen = $_GET['id_dosen'];

$query = "SELECT * FROM dosen WHERE id_dosen = $id_dosen";

$result = mysqli_query($connect, $query);

$row = mysqli_fetch_assoc($result);


<!DOCTYPE html>

<html>
<head>
<h1>Ubah Data Dosen</h1>
</head>
<body>

<form action="update.php" method="post">
    <table>
    <tr>
        <td><label for="nama">Nama dosen</label></td>
        <td>:</td>
        <td><input type="text" name="nama_dosen" value="<?php echo $row['nama_dosen']; ?>" ></td>
    </tr>
    <tr>
        <td><label for="no_telp">No. Telepon </label></td>
        <td>:</td>
        <td><input type="text" name="telp" id="no_telp" value="<?php echo $row['telp']; ?>"></td>
    </tr>
    <tr>
        <td></td>
        <td><input type="hidden" name="id_dosen" value="<?php echo $row['id_dosen'];?>"></td>
        <td><input type="submit" value="Simpan" name="btnSimpan"></td>
    </tr>
    </table>
</form>
    
</body>
</html>
    
   4. Berikan code query untuk mengupdate sebuah data yang ada pada ke database?


include '../connect.php';

$id_dosen = $_GET['id_dosen'];

$query = "SELECT * FROM dosen WHERE id_dosen = $id_dosen";

$result = mysqli_query($connect, $query);

$row = mysqli_fetch_assoc($result);



<!DOCTYPE html>

<html>
<head>
<h1>Ubah Data Dosen</h1>
</head>
<body>

<form action="update.php" method="post">
    <table>
    <tr>
        <td><label for="nama">Nama dosen</label></td>
        <td>:</td>
        <td><input type="text" name="nama_dosen" value="<?php echo $row['nama_dosen']; ?>" ></td>
    </tr>
    <tr>
        <td><label for="no_telp">No. Telepon </label></td>
        <td>:</td>
        <td><input type="text" name="telp" id="no_telp" value="<?php echo $row['telp']; ?>"></td>
    </tr>
    <tr>
        <td></td>
        <td><input type="hidden" name="id_dosen" value="<?php echo $row['id_dosen'];?>"></td>
        <td><input type="submit" value="Simpan" name="btnSimpan"></td>
    </tr>
    </table>
</form>
    
</body>
</html>

5. Berikan code query untuk menghapus sebuah data yang ada pada ke database?


include '../connect.php';

$id_dosen = $_GET['id_dosen'];

$query = "DELETE FROM dosen WHERE id_dosen = $id_dosen";

$result = mysqli_query($connect, $query);

$num = mysqli_affected_rows($connect);


if($num > 0)
{
    echo "Berhasil hapus data <br>";

}else{
    echo "Gagal hapus data <br>";
}

echo "<a href='read.php'>Lihat Data</a>";

data awal
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/data_awal.png)

hapus data 1
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/hapus_data1.png)

hapus data 2
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/hapus_data2.png)

hapus data 3
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/hapus_data3.png)

tambah data 1
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/tambah_data1.png)

tambah data 2
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/tambah_data2.png)

tambah data 3
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/tambah_data3.png)

update data 1
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/update_data1.png)

update data 2
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/update_data2.png)

update data 3
![alt text](https://github.com/Lunggita29/AmeliaLunggita_Modul7_bg1_bg2/blob/master/update_data3.png)

