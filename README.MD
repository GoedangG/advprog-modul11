## ADVPROG - Modul 11

### Rizqi Bayu Utama - 2206826330

1. Compare the application logs before and after you exposed it as a Service. Try to open the app several times while the proxy into the Service is running. What do you see in the logs? Does the number of logs increase each time you open the app?
[](img/1.png)

    > Setiap kali saya membuka app, maka akan men-trigger method `GET` 2 kali setiap membuka.

2. Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to `kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you explicitly created?
    > -n di `kubectl` membantu kita untuk men-spesifik area yang akan kita lihat. Jika kita tidak menemukan `pods` atau `services` yang telah kita buat tanpa menggunakan `-n`, mungkin karena `pods` dan `services` tersebut tidak berada pada area `default` yang mana membutuhkan `-n` untuk men-specified.