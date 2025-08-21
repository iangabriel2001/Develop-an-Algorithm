
# Login System with Approved Users and Devices

This project demonstrates a simple login validation system in Python.  
It checks whether a given `username` belongs to a list of approved users and whether the provided `device_id` matches the assigned device for that user.

---

## 🚀 Features
- Validates if a username is approved.
- Ensures the correct device is used for login.
- Provides clear messages for:
  - Approved user with correct device ✅
  - Approved user with wrong device ⚠️
  - Unapproved user ❌

---

## 📂 Project Structure
.
├── login_system.py # Main Python script
└── README.md # Project documentation

python
Copy
Edit

---

## 📝 Example Code

```python
# Approved users and devices
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

# Define login function
def login(username, device_id):
    if username in approved_users:
        print("The user", username, "is approved to access the system.")
        ind = approved_users.index(username)
        if device_id == approved_devices[ind]:
            print(device_id, "is the assigned device for", username)
        else:
            print(device_id, "is not their assigned device.")
    else:
        print("The username", username, "is not approved to access the system.")

# Example calls
login("sgilmore", "4n482ts")   # Approved, correct device
login("sgilmore", "hl0s5o1")   # Approved, wrong device
login("not_a_user", "random1") # Not approved
🖥️ Sample Output
pgsql
Copy
Edit
The user sgilmore is approved to access the system.
4n482ts is the assigned device for sgilmore
-----
The user sgilmore is approved to access the system.
hl0s5o1 is not their assigned device.
-----
The username not_a_user is not approved to access the system.
