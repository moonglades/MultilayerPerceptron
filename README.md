# Multilayer-Perceptron

Perceptron, jaringan saraf yang namanya membangkitkan bagaimana masa depan tampak dari perspektif tahun 1950-an, adalah algoritma sederhana yang dimaksudkan untuk melakukan klasifikasi biner; yaitu memprediksi apakah input termasuk dalam kategori minat tertentu atau tidak (mis: penipuan/bukan penipuan).

Perceptron adalah pengklasifikasi linier — algoritma yang mengklasifikasikan input dengan memisahkan dua kategori dengan garis lurus. Input biasanya berupa vektor fitur x dikalikan dengan bobot w dan ditambahkan ke bias b: y = w * x + b.

Perceptron menghasilkan output tunggal berdasarkan beberapa input bernilai nyata dengan membentuk kombinasi linier menggunakan bobot input (dan terkadang melewatkan output melalui fungsi aktivasi non-linier).

Rosenblatt membangun perceptron satu lapis; itu tidak termasuk banyak lapisan, yang memungkinkan jaringan saraf untuk memodelkan hierarki fitur. Oleh karena itu, jaringan saraf dangkal, yang akhirnya mencegah perceptronnya melakukan klasifikasi non-linear, seperti fungsi logika XOR klasik (pemicu operator XOR ketika input menunjukkan salah satu sifat atau lainnya, tetapi tidak keduanya; itu berdiri untuk “eksklusif ATAU”).

Maju cepat ke 1986, ketika Hinton, Rumelhart, dan Williams menerbitkan sebuah makalah "Mempelajari representasi dengan kesalahan propagasi balik", memperkenalkan konsep propagasi balik dan lapisan tersembunyi - oleh karena itu dapat dikatakan melahirkan Multilayer Perceptrons (MLPs):

Backpropagation, prosedur untuk menyesuaikan bobot berulang kali sehingga meminimalkan perbedaan antara output aktual dan output yang diinginkan
Hidden Layers, yang merupakan node neuron yang ditumpuk di antara input dan output, memungkinkan jaringan saraf untuk mempelajari fitur yang lebih rumit (seperti logika XOR)
Oleh karena itu, MLP dapat dianggap sebagai jaringan saraf tiruan yang dalam. Ini terdiri dari lebih dari satu perceptron. Mereka terdiri dari lapisan input untuk menerima sinyal, lapisan output yang membuat keputusan atau prediksi tentang input, dan di antara keduanya, sejumlah lapisan tersembunyi yang merupakan mesin komputasi sebenarnya dari MLP.

Perceptron multilayer berlatih pada satu set pasangan input-output dan belajar untuk memodelkan korelasi (atau ketergantungan) antara input dan output tersebut. Pelatihan melibatkan penyesuaian parameter, atau bobot dan bias, dari model untuk meminimalkan kesalahan. Backpropagation digunakan untuk membuat penyesuaian bobot dan bias relatif terhadap kesalahan, dan kesalahan itu sendiri dapat diukur dengan berbagai cara, termasuk dengan root mean squared error (RMSE).

Jaringan feedforward seperti MLP sama seperti ping-pong: mereka terutama terlibat dalam dua gerakan, bolak-balik yang konstan (operan maju dan mundur):

. Pada lintasan maju, aliran sinyal bergerak dari lapisan masukan melalui lapisan tersembunyi ke lapisan keluaran, dan keputusan lapisan keluaran diukur terhadap label kebenaran dasar;

. Dalam lintasan mundur, menggunakan perambatan balik dan aturan rantai kalkulus, turunan parsial dari fungsi kesalahan mengenai berbagai bobot dan bias dipropagasi mundur melalui MLP. Tindakan diferensiasi itu memberi kita gradien, atau lanskap kesalahan, di mana parameter dapat disesuaikan saat mereka memindahkan MLP satu langkah lebih dekat ke kesalahan minimum. (ini dapat dilakukan dengan algoritma optimasi berbasis gradien seperti penurunan gradien stokastik).

Jaringan terus memainkan permainan ping-pong itu sampai kesalahannya tidak berkurang. Keadaan ini dikenal sebagai konvergensi.

![MLP](https://www.researchgate.net/profile/Mohamed_Zahran6/publication/303875065/figure/fig4/AS:371118507610123@1465492955561/A-hypothetical-example-of-Multilayer-Perceptron-Network.png)

