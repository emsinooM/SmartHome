# SmartHome
## Prerequisites
Create a MongoDB Atlas cluster.<br>
Create a database called sensors_db with a collection sensors<br>
Prepare your database by adding the sample records in your collection. Please see the writeup.<br>

## Steps on how to run the Rest API
1. Open the project in Visual Studio Code and then open a new terminal. Create a virtual environment using the below command

    ```sh
    # Windows
    py -m venv .venv
    # Linux
    python -m venv .venv
    ```

2. Activate the virtual environment

    ```sh
    # Windows
    .\.venv\Scripts\activate
    # Linux
    source .venv/bin/activate
    ```

3. Install the dependencies

    ```sh
    pip install -r requirements.txt
    ```
4. Rename the .env.local to .env

    ```sh
    mv .env.local .env
    ```

5. Replace the value of the .env file to your MongoDB Atlas

    ```sh
    MONGO_DB_CONN_STRING=mongodb+srv://<DB_USER_NAME>:<DB_PASSWORD>@<MONGO_DB_ATLAS_ENDPOINT>/sensors_db
    ```

6. Run the Flask server

    ```sh
    flask run
    ```

7. Open your browser and type the following URL

    ```sh
    http://<IP>:5000
    ```

