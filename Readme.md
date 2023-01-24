# Belajar Apache Maven
Maven merupakan salah satu tools build automation yang populer untuk java programmer
dengan tool ini memudahkan kita untuk melakukan berbagai tasks manual menjadi automation seperti
dependency management, distribution file dll.

# Membuat project di maven
Untuk membuat project di maven kita harus terhubung dengan internet karena resource yang akan digunakan harus didownlaod terlebih dahulu
untuk membuat project di maven kita bisa jalankan perintah  berikut:
- mvn archetype:generate
- maven-archetype-quickstart

# maven Lifecycle
Beberapa perintah lifecycle maven

- clean, menghapus folder target (tempat menyimpan hasil kompilasi)
- compile, untuk melakukan kompilasi source code project
- test-compile, untuk melakukan kompilasi source code project
- test, untuk menjalankan unit test
- package, untuk membuat distribution file aplikasi
- install, untuk menginstalll project ke local repository, sehigga bisa digunakan di project lain di local
- deploy,  deploy project ke remote repository di server

untuk manjalankan lifecycle di maven bisa dilakukan secara bersamaan seperti:
- mvn compile test-compile clean package
  
# Dependency source
Aplikasi yang kita buat terkadang membutuhkan beberapa library, daripada kita harus buat dari awal kita bisa gunakan library third party
untuk memepercepat proses development aplikasi, kita bisa mencari library tambahan di link berikut:
- https://search.maven.org/
- https://mvnrepository.com/

# Maven properties
ketika kita membuat project maven kita akan menenmukan file pom.xml
di dalam file tersebut kitya akan menemukan tag <properties> dimana di dalam tag ini kita bisa membuat properties
untuk tujuan menyimpan konfigurasi dari aplikasi kita sehingga kita tidak perlu menambahkan file konfigurasi secara hardcode

# Distribution file
- untuk melakukan pendistribusia aplikasi bisa menggunakan
  salah plugin yaitu assembly plugin, dan masih banyak plugin lain bisa digunakan ini ahanya salah satu diantaranya
  dokumentasi penggunaan plugin ada di link berikut https://maven.apache.org/plugins/maven-assembly-plugin/usage.html
  - untuk melakukan build aplikasi kita cukup menjalankan perintah:
  mvn package assembly:single
    
# Multi module project