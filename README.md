- main_crate starts both exercises
- steps for testing blockchaing_simulator:
    1. install websocat
    2. run this command to connect to websocket: websocat ws://127.0.0.1:7879/ws
 
- steps for testing blockchain_client_server exercise:
    1. run this command which writes Block_1 to database:
echo '{"index_id":1,"timestamp":1680000000,"transactions":"Alice pays Bob 10 coins","nonce":12345,"hash":"MilanIsRustacean","previous_hash":"000000000000"}' | tr -d '\r\n' | websocat ws://127.0.0.1:7878/
  2. run this command to send http request and to read Block_1 hash from database: curl "http://127.0.0.1:7878/hash?block_id=1"
