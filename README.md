# 🏥 Patient Management System API

A RESTful API built with **FastAPI** to manage patient health records. Supports viewing, filtering, and sorting patients based on health metrics like BMI, height, and weight.

---

## 🚀 Tech Stack

- **Python** 3.x
- **FastAPI**
- **Uvicorn** (ASGI server)
- **JSON** (local data storage)

---

## 📁 Project Structure

```
FastAPI/
├── main.py          # Main FastAPI application
├── patients.json    # Patient records database
└── README.md
```

---

## ⚙️ Setup & Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/Parthbiru/FastAPI.git
cd FastAPI
```

**2. Create and activate virtual environment**
```bash
python -m venv myenv
myenv\Scripts\activate      # Windows
source myenv/bin/activate   # Mac/Linux
```

**3. Install dependencies**
```bash
pip install fastapi uvicorn
```

**4. Run the server**
```bash
uvicorn main:app --reload
```

**5. Open in browser**
```
http://127.0.0.1:8000
http://127.0.0.1:8000/docs   ← Swagger UI (interactive docs)
```

---

## 📌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Welcome message |
| GET | `/about` | About the API |
| GET | `/view` | Get all patient records |
| GET | `/patients/{patient_id}` | Get a specific patient by ID |
| GET | `/sort` | Sort patients by height, weight, or BMI |

---

## 🔍 Example Usage

**Get a specific patient**
```
GET /patients/P001
```
```json
{
  "name": "Rahul Sharma",
  "city": "Ahmedabad",
  "age": 28,
  "gender": "Male",
  "height": 170,
  "weight": 68,
  "bmi": 23.5,
  "verdict": "Normal"
}
```

**Sort patients by BMI (descending)**
```
GET /sort?sort_by=bmi&order=desc
```

**Sort patients by weight (ascending)**
```
GET /sort?sort_by=weight&order=asc
```

---

## 🗃️ Patient Data Fields

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Patient full name |
| `city` | string | City of residence |
| `age` | integer | Age in years |
| `gender` | string | Male / Female |
| `height` | float | Height in cm |
| `weight` | float | Weight in kg |
| `bmi` | float | Body Mass Index |
| `verdict` | string | Normal / Overweight / Obese |

---

## 👨‍💻 Author

**Parth Biru**  
BCA Graduate | Aspiring Full Stack Developer  
[GitHub](https://github.com/Parthbiru)
