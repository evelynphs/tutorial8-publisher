a. How many data your publlsher program will send to the message broker in one run? <br>

   Dalam satu kali run, method `main` akan dipanggil satu kali. Dalam method `main`, terdapat 5 kali pemanggilan method `publish_event` sehingga dalam satu kali run akan dikirim 5 data.

<br>

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? <br>
   
   URL yang sama pada publisher dan subscriber berarti bahwa keduanya terhubung ke message broker yang sama menggunakan standar AMQP. Baik subscriber maupun publisher terhubung ke message broker dengan kredensial yang sama menggunakan `guest` sebagai username dan password. Message broker tersebut dijalankan pada `localhost` (pada mesin tempat program dijalankan), spesifiknya pada port `5672`.

<br>
<br>

### Running RabbitMQ as message broker
![First run rabbitmq screen capture](/assets/images/running-rabbit-mq1.png)