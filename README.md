<h1 align="center" >
  Point Of Sale app
</h1>

### Overview
This project introduces a **custom Point of Sale (POS)** page built for ERPNext, specifically designed to work in offline mode. The default ERPNext POS system lacks robust offline support, so this custom solution allows sales transactions to continue smoothly even without internet connectivity.

The custom POS page comes pre-installed when you install the app, requiring no manual setup.

<br>

### the way it works :
I'm working with a custom POS implementation in ERPNext, using offline storage by managing variables in memory (RAM) to simulate POS operations. I'm fetching necessary data (like customers, items, item prices, and warehouse lists) at the start, storing them in arrays and maps, and then operating offline with this data. My approach aligns well with handling offline functionality, especially in POS systems that need to operate without continuous server interaction.

### POS PAGE overview :
| Tab | photo |
|-----|-------|
|POS Screen             | ![screen1](https://github.com/user-attachments/assets/8203e211-a192-476c-882c-a40cbe0a7f79)|
|Select ItemGroup       | ![screen2](https://github.com/user-attachments/assets/1fd57f82-19af-44dd-8cae-a19dd4f36515)|
|Get All Item (Filtred) | ![screen3](https://github.com/user-attachments/assets/5854b6cc-7a35-4f05-843f-2c1037819ada)|
|Selecting customer     | ![screen4](https://github.com/user-attachments/assets/43698fd7-1f24-44d8-a3d2-77e148b2a9e9)|
|Click on Item to sell  | ![screen5](https://github.com/user-attachments/assets/99e2ecb9-2b70-4263-84d0-fcac043fb5a4)|
|Item Details Cart      | ![screen6](https://github.com/user-attachments/assets/a3cc0681-975d-4e11-bed8-6155a7421259)|



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
