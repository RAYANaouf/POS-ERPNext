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
|POS Screen             | ![screen1](https://github.com/user-attachments/assets/c5bb1230-5e09-4fcb-b727-4000ceeb90bf)|
|Select ItemGroup       | ![screen2](https://github.com/user-attachments/assets/8a97c052-cd45-47f4-95fc-1e90bd0aa332)|
|Get All Item (Filtred) | ![screen3](https://github.com/user-attachments/assets/f2b8200a-207a-449b-a00b-13f7a5fc5280)|
|Selecting customer     | ![screen4](https://github.com/user-attachments/assets/c11af200-2cdd-4ffe-9ba6-40a534e0fd08)|
|Click on Item to sell  | ![screen5](https://github.com/user-attachments/assets/a8edfd1d-057f-458b-ae9a-f1a3f3b7a949)|
|Item Details Cart      | ![screen6](https://github.com/user-attachments/assets/9099d926-259b-4900-93eb-1bb7e5122785)|
|When Checkout          | ![screen7](https://github.com/user-attachments/assets/13d15f8e-e7d1-4c57-8a8a-82bc44ea42aa)|



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
