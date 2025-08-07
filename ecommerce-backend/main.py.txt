from flask import Flask, jsonify
from flask_cors import CORS

app = Flask(__name__)
CORS(app)

@app.route("/api/products")
def products():
    return jsonify([
        {"id": 1, "name": "Ghost Tee", "price": 25},
        {"id": 2, "name": "Energy Hoodie", "price": 45},
        {"id": 3, "name": "Phantom Shirt", "price": 35}
    ])

if __name__ == "__main__":
    app.run(debug=True)
