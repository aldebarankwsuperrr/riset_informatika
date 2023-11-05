# Topik Penelitian
## Pemanfaatan Machine Learning dalam Pengkategorian Kesegaran Buah
### Problem Statement
Kesegaran buah merupakan salah satu aspek penting yang dipertimbangkan dalam penjualan buah. Mungkin kita sebagai manusia dapat secara langsung membedakan mana buah yang segar dan buah yang kurang segar. Namun pengkategorian kesegaran buah yang manual menggunakan tenaga manusia memiliki beberapa kekurangan seperti kestabilan kinerja dan kecepatan. Oleh karena itu, dibutuhkan sebuah alat pembantu yang dapat menutupi kekurangan metode pengkategorian manual, salah satu teknologi yang dapat dimanfaatkan adalah YOLOv8 dan ResNet. Dengan memanfaatkan YOLOv8 dan ResNet proses pengkateogrian diharapkan menjadi lebih cepat dan stabil dibandingkan metode manual.
### Research Question
- Bagaimana implementasi YOLOv8 dan ResNet dapat digunakan untuk mengkategorikan kesegaran buah secara otomatis?
- Bagaimana tingkat kecepatan pengkategorian kesegaran buah menggunakan YOLOv8 dan ResNet dibandingkan dengan pengkategorian manual?
- Bagaimana tingkat akurasi pengkategorian kesegaran buah dengan menggunakan YOLOv8 dan ResNet, dan bagaimana memperbaiki akurasi tersebut jika diperlukan?
### Literature Review
- Xiao, B., Nguyen, M. & Yan, W.Q. Fruit ripeness identification using YOLOv8 model. Multimed Tools Appl (2023).
- Terven, J., & Cordova-Esparza, D. (2023). A Comprehensive Review of YOLO: From YOLOv1 and Beyond. arXiv, 2304.00501
- Devvi Sarwinda, Radifa Hilya Paradisa, Alhadi Bustamam, Pinkie Anggia, Deep Learning in Image Classification using Residual Network (ResNet) Variants for Detection of Colorectal Cancer, Procedia Computer Science, Volume 179, 2021, Pages 423-431, ISSN 1877-0509.
#### Method - Methodology
##### Methodology
- Yunong Tian, Guodong Yang, Zhe Wang, Hao Wang, En Li, Zize Liang, Apple detection during different growth stages in orchards using the improved YOLO-V3 model, Computers and Electronics in Agriculture, Volume 157, 2019, Pages 417-426, ISSN 0168-1699, https://doi.org/10.1016/j.compag.2019.01.012.
##### Method
- Puzhen Wu, Han Weng, Wenting Luo, Yi Zhan, Lixia Xiong, Hongyan Zhang, Hai Yan, An improved Yolov5s based on transformer backbone network for detection and classification of bronchoalveolar lavage cells, Computational and Structural Biotechnology Journal, Volume 21, 2023, Pages 2985-3001, ISSN 2001-0370, https://doi.org/10.1016/j.csbj.2023.05.008.

### Methodology
#### YOLOv8
YOLO (You Only Look Once) merupakan sebuah algoritma deteksi objek yang menawarkan kecepatan deteksi dengan merubah permasalahan deteksi kedalam sebuah permasalahan regresi. 

![YOLO](https://th.bing.com/th/id/R.c67a4bffde7dd6f7c0371ae5e705e0f8?rik=FRrcZc%2fLaDWtTQ&riu=http%3a%2f%2fmedia5.datahacker.rs%2f2019%2f04%2fyolo_diagram-1920x1043.jpg&ehk=LEAYbZGLSfZRGYgdndadDEMZQ0T0g3Ylp0j1GUKISoc%3d&risl=&pid=ImgRaw&r=0)

YOLOv8 adalah versi terbaru dari YOLO oleh Ultralytics. Sebagai model state-of-the-art (SOTA) yang terkini, YOLOv8 membangun atas kesuksesan versi sebelumnya, memperkenalkan fitur-fitur baru dan perbaikan untuk kinerja, fleksibilitas, dan efisiensi yang lebih baik. YOLOv8 mendukung berbagai tugas kecerdasan visual, termasuk deteksi, segmentasi, estimasi pose, pelacakan, dan klasifikasi. Keunggulan ini memungkinkan pengguna memanfaatkan kemampuan YOLOv8 dalam berbagai aplikasi dan domain yang berbeda.

#### ResNet
ResNet, yang diusulkan pada tahun 2015 oleh peneliti di Microsoft Research, memperkenalkan arsitektur baru yang disebut ResNet. Untuk mengatasi masalah gradien yang menghilang/meledak, arsitektur ini memperkenalkan konsep yang disebut Blok Residual. Dalam ResNet, kita menggunakan teknik yang disebut koneksi lewat (skip connections). Koneksi lewat menghubungkan aktivasi lapisan ke lapisan selanjutnya dengan melewati beberapa lapisan di antaranya. Hal ini membentuk blok residual. ResNet dibentuk dengan menyusun blok-blok residual ini bersama-sama. Pendekatan di balik ResNet adalah daripada lapisan-lapisan mempelajari pemetaan dasar, kita memungkinkan jaringan untuk sesuai dengan pemetaan residual. Jadi, daripada mengatakan H(x), pemetaan awal, kita biarkan jaringan sesuai,

![ResNet](https://media.geeksforgeeks.org/wp-content/uploads/20200424011510/Residual-Block.PNG)

Keuntungan dari menambahkan jenis koneksi lewat ini adalah bahwa jika salah satu lapisan merusak kinerja arsitektur, maka lapisan tersebut akan dilewati oleh regulasi. Dengan demikian, ini menghasilkan pelatihan jaringan saraf yang sangat dalam tanpa masalah yang disebabkan oleh gradien yang menghilang/meledak.
