# OCR Alphabet Classification Project
## Cara Menjalankan Docker TensorFlow Serving
1. Jalankan perintah berikut untuk menjalankan Docker container dan memasukkan direktori **saved_model** dari path yang sesuai:

    ```bash
    docker run -it --rm -p 8502:8502 -v C:/tmp/BPML/saved_model:/models/saved_model --entrypoint /bin/bash tensorflow/serving
    ```

2. Setelah berada di dalam container, jalankan TensorFlow Model Server dengan perintah berikut:

    ```bash
    tensorflow_model_server --rest_api_port=8502 --model_name=saved_model --model_base_path=/models/saved_model/
    ```

3. Akses model melalui TensorFlow Serving REST API di URL berikut:

    ```
    http://localhost:8502/v1/models/saved_model
    ```

## Cara Mengaktifkan Environment untuk kernel Requests TFserving
Pada Terminal :
    ```
    .venv\Scripts\activate
    ```
