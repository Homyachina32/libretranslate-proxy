from flask import Flask, request, jsonify
import requests

app = Flask(__name__)

@app.route('/translate', methods=['POST'])
def translate():
    data = request.json
    response = requests.post(
        'https://translate.argosopentech.com/translate',
        json=data,
        timeout=10
    )
    return jsonify(response.json())

@app.route('/')
def home():
    return "LibreTranslate Proxy is running!"

if __name__ == "__main__":
    app.run(host='0.0.0.0', port=5000)
