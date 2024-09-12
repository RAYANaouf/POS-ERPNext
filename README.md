<h1 align="center" >
  Point Of Sale app
</h1>

### Overview
This project introduces a **custom Point of Sale (POS)** page built for ERPNext, specifically designed to work in offline mode. The default ERPNext POS system lacks robust offline support, so this custom solution allows sales transactions to continue smoothly even without internet connectivity.

The custom POS page comes pre-installed when you install the app, requiring no manual setup.

<br>

### POS PAGE overview :
| Tab | photo |
|-----|-------|
|POS Screen             | ![screen1](https://github.com/user-attachments/assets/dd15895b-ff91-464d-9046-b30c75256b6b)|
|Select ItemGroup       | ![screen2](https://github.com/user-attachments/assets/539843ac-1886-4129-b245-a8d3cea87bb2)|
|Get All Item (Filtred) | ![screen3](https://github.com/user-attachments/assets/d0d72e4f-b6c2-4ed2-8b6d-1614ab9d8a68)|
|Selecting customer     | ![screen4](https://github.com/user-attachments/assets/43698fd7-1f24-44d8-a3d2-77e148b2a9e9)|
|Click on Item to sell  | ![screen5](https://github.com/user-attachments/assets/c964b503-b4be-4786-9829-fc1b7aa27db0)|
|Item Details Cart      | ![screen6](https://github.com/user-attachments/assets/88e205c2-a9d8-4164-88b9-683c8d870aaa)|



### Features
- **Offline Mode Support**: Perform sales and manage transactions even without an internet connection. Data will automatically sync once the connection is restored.
- **User-Friendly Interface**: A simple, responsive, and efficient POS interface that works seamlessly in both online and offline modes.
- **Local Inventory Caching**: Product and inventory data is cached locally, allowing users to search and add items without needing an active connection.
- **Auto-Sync**: Offline transactions are synced with the ERPNext backend as soon as the internet is available, ensuring smooth reconciliation of offline sales data.
- **Integrated into ERPNext**:No manual page setup is required. The POS page is automatically installed with the app.

### Installation
To install the **Halfware App** on your Frappe or ERPNext instance: 
1. **Clone the repository** : 
```bash
$ bench get-app https://github.com/RAYANaouf/ERPNEXT-POS
```
2. **Install the app**:

Go to the directory where your ERPNext instance is set up:
```bash
cd /path/to/frappe-bench
```
Then install the app into your ERPNext site:

```bash
bench get-app  
bench --site [your-site-name] install-app ERPNEXT-POS
```
