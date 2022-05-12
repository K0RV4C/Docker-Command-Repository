Docker command

docker ls เป็นคําสั่งดูว่าขณะนี้มี  container ตัวไหนรันอยู่บ้าง รูปแบบการใช้คําสั่งคือ
docker ls

docker images เป็นคําสั่งดูว่าในเครื่องเรามี Image อะไรอยู่บ้าง หมายถึง image ที่ pull มาอยู่บนเครื่องเราแล้ว วิธีใช้คือ
docker images

docker rm เป็นทําสั่งสําหรับลบ container รูปแบบการใช้งานทําสั่งคือ
docker rm [ชื่อ หรือid ของ container]

***จะลบได้เฉพาะ container ที่ stop อยู่เท่านั้น ถ้าต้องการลบ container ที่กําลังรันอยู่ ให้เพิ่ม option -f เข้าไป 4. docker rmi เป็นคําสั่งลบ image ที่อยู่ในเครื่อง รูปแบบคําสั่งคือ
docker rmi [ชื่อ หรือid ของ image ที่จะลบ]

***จะไม่สามารถลบ Image ที่มี container รันอยู่ได้ 5. docker run เป็นคําสั่ง run container รูปแบบการใช้งานคําสั่งคือ
docker run [option] [ชื่อ image] [command]
[option] คือ option ต่างๆ เช่น -p คือ map port ฯลฯ
[ชื่อ image] คือ ชื่อของ image ที่เราจะ run
[connamd] คือ command ที่ต้องการทํา เมื่อ container start แล้ว
ตัวอย่าง
docker run --name some-nginx -v /some/content:/usr/share/nginx/html:ro -d nginx

docker start คําสั่ง start container วิธีใช้คือ
docker start [ชื่อ container]

docker stop คําสั่ง stop container วิธีใช้คือ
docker stop [ชื่อ container]

docker stats คําสั่งใช้ดูการใช้ Resource ของแต่ละ Containner (CPU, RAM) รูปแบบการใช้คือ
docker stats
