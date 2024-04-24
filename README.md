a. How many data your publlsher program will send to the message broker in one run? <br>

   Dalam satu kali run, method `main` akan dipanggil satu kali. Dalam method `main`, terdapat 5 kali pemanggilan method `publish_event` sehingga dalam satu kali run akan dikirim 5 data.

<br>

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? <br>
   
   URL yang sama pada publisher dan subscriber berarti bahwa keduanya terhubung ke message broker yang sama menggunakan standar AMQP. Baik subscriber maupun publisher terhubung ke message broker dengan kredensial yang sama menggunakan `guest` sebagai username dan password. Message broker tersebut dijalankan pada `localhost` (pada mesin tempat program dijalankan), spesifiknya pada port `5672`.

<br>
<br>

### Running RabbitMQ as message broker
![First run rabbitmq screen capture](/assets/images/running-rabbit-mq1.png)

<br>

### Sending and processing event
![Sending and processing event](/assets/images/console1.png)
ketika menjalankan `cargo run` pada subscriber, program akan menyalakan receiver yang siap menerima message dari message broker. Ketika menjalankan `cargo run` pada publisher, program akan mengirimkan message ke message broker menggunakan `publish_event`. Message tersebut berisi lima data `user_id` dan `user_name` yang berbeda-beda. Program subscriber akan menerima message tersebut melalui message broker, kemudian mencetak (print) pesan sesuai format yang ada pada method `UserCreatedHandler`. Program subscriber mencetak pesan sebanyak lima kali sesuai jumlah message yang diterima. Ini menandakan bahwa komunikasi antara subscriber dan publisher berjalan dengan baik melalui perantara message broker.

