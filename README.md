# modul-3
###### Nama: Jenissa ananda yoanita 
###### Kelas: XII RPl 1
###### No Absen: 30

###### Route dengan aksi controller
Route seperti ini ketika dijalankan akan mengakses controller yang disebutkan pada
parameter kedua. Jika ingin mengakses method atau function tertentu pada controller, maka
antara nama controller dengan nama fungsi dipisahkan denan tanda @. Untuk 
memepraktekkan route ini buatlah satu controller dengan menggunakan perintah artisan sebagai 
berikut:
``` php artisan make:controller BarangController
```

Perintah artisan diatas 
akan menghasilkan satu file baru bernama ProdukController.php yang terletak difolder
app\Http\Controller. Bukalah file controller tersebut dan tambahkan satu fungsi bernama 
index seperti pada contoh skrip dibawah:
```
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;
use illuminate\Routing\Route;


class BarangController extends Controller
{
    public function index()
    {
        return 'Mengakses Fungsi di controller menggunakan route';
    }  
    ```
    Kemudian buka file web.php yang ada pada folder routes/web.php tambahkan satu route baru 
    dengan bentuk seperti berikut:
    ```
    <?php

use illuminate\Support\Facades\Route;
use App\Http\Controllers\BarangController;
use App\Http\Controllers\KategoriController;

Route::get('/barang', [BarangController::class, 'index']);
```
Tapi sebelum membuat itu semua kita herus memasukkan code program dicmd, dengan code seperti dibawah ini. Agar website kita berjalan.
![image](https://user-images.githubusercontent.com/109930527/182108585-22a1caa9-808b-4a14-902e-bf350f91eda2.png)

![image](https://user-images.githubusercontent.com/109930527/182108803-447e416d-c707-4481-afe5-7dfd1d3162bf.png)

SOAL
1. Buatlah Route yang menuju kehalaman kategori 
2. Buatlah halaman tambahan data diatas 
