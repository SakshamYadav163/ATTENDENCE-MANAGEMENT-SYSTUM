# ATTENDENCE-MANAGEMENT-SYSTUM
## Attendance Management System (Java Swing + MySQL)

### Prerequisites
- Java 17+
- Maven
- MySQL Server

### Setup
1. Create database and sample data:
   - Run `src/main/resources/sql/attendance_system.sql` in MySQL.
2. Configure DB credentials:
   - Edit `src/main/resources/application.properties` (`db.user`, `db.password`).
3. Build & run:
```
mvn clean package
java -jar target/attendance-management-system-1.0.0-jar-with-dependencies.jar
```

### Sample Logins
- Teacher: `alice` / `alice123`
- Student: `charlie` / `charlie123`

### Features
- Teacher: Generate QR (sessionId, course, timestamp, location), view attendance, export Excel.
- Student: Scan QR from image, 15m location validation, mark attendance, view history.
- Tech: Swing UI, ZXing, Apache POI, MySQL JDBC, Haversine formula.

### Notes
- Location uses stored coordinates to simulate GPS for both roles.
- QR images saved to `output/qrcodes/`.

### Example Outputs
- QR generated PNG under `output/qrcodes/`.
- Export confirmation dialog after saving `.xlsx`.


