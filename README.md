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
|POS Screen                         | ![screen1](https://github.com/user-attachments/assets/3df75b3a-f4ae-4f27-a3b9-bad2c3df8517)|
|Select ItemGroup                   | ![screen2](https://github.com/user-attachments/assets/329f88e2-793a-4c1c-82ee-1c2423fa7f47)|
|Get All Item (Filtred by name,code bar or group)             | ![screen3](https://github.com/user-attachments/assets/a170915f-1fdc-4472-ba18-5e1556943930)|
|Selecting items                    | ![screen4](https://github.com/user-attachments/assets/b3e7cdee-30ce-4b56-8356-e5e03a1fd78f)|
|select client and price list to detect item price              | ![screen5](https://github.com/user-attachments/assets/d180966c-8ea2-419c-a78f-e71373ef6846)|
|Item Details Cart                  | ![screen6](https://github.com/user-attachments/assets/9099d926-259b-4900-93eb-1bb7e5122785)|
|When Checkout                      | ![screen7](https://github.com/user-attachments/assets/13d15f8e-e7d1-4c57-8a8a-82bc44ea42aa)|
|Submit the pos invoice (on local)  | ![screen8](https://github.com/user-attachments/assets/b16197c9-5b5e-4e67-9f94-d68844656db0)|
|after submit **create new tab** && **make sync button orange** | ![screen9](https://github.com/user-attachments/assets/e1cd51c6-73fa-4237-b9d5-d8a3e4474f5a)|
|Sync with progress bar             | ![screen10](https://github.com/user-attachments/assets/74f5c087-61ab-485e-aa6f-16b7d39c2ca0)|
|after sync the button return green | ![screen11](https://github.com/user-attachments/assets/3bb58dec-23a0-4036-9029-875b528c4b52)|
|menu options                       | ![screen12](https://github.com/user-attachments/assets/490021e5-e72e-44b6-8599-2df709e65c96)|






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
