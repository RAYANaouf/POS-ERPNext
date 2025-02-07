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
|POS Screen                         | ![screen1](https://github.com/user-attachments/assets/0c20ab4c-d69f-4e77-8195-6bdca0f973bd)|
|Select ItemGroup                   | ![screen2](https://github.com/user-attachments/assets/329f88e2-793a-4c1c-82ee-1c2423fa7f47)|
|Get All Item (Filtred by name,code bar or group)             | ![screen3](https://github.com/user-attachments/assets/d44ecd0e-18e3-4ed4-94c5-c5aacce9fe88)|
|Selecting items                    | ![screen4](https://github.com/user-attachments/assets/ee198c63-8bdd-47dd-8667-6e39aa3baabc)|
|select client and price list to detect item price              | ![screen5](https://github.com/user-attachments/assets/d180966c-8ea2-419c-a78f-e71373ef6846)|
|Item Details Cart : quantity Rate (can change it) , Discount persentage or amount calculated based on each other. price list rate just to show the base rate that came from price list. and we have the calculated field discount  amount.                    | ![screen6](https://github.com/user-attachments/assets/fd98b052-90fd-4efa-a21b-ddc72499295d)|
|When Checkout : enter the paid amount , detect if the pos is Paid or Unpaid and calculate To change amount                     | ![screen7](https://github.com/user-attachments/assets/4d3f379b-b10f-41b0-8d50-89cab9523cf3)|
|Submit the pos invoice (if the pos is unpaid it will push it diractly to the server so the internet conection is required otherwise it will save on the local db)  | ![screen8](https://github.com/user-attachments/assets/aa9e31dc-57f7-4c57-b4eb-2af865431a7e)|
|after submit **create new tab** && **make sync button orange showing unsynced pos** | ![screen9](https://github.com/user-attachments/assets/b0e0eeb4-776d-454e-83e4-f2d5a605e474)|
|Sync with progress bar             | ![screen10](https://github.com/user-attachments/assets/d5375c99-dd45-4afb-8b62-111eb93777a5)|
|after sync the button return green | ![screen11](https://github.com/user-attachments/assets/13e05d96-abed-48cb-9aa6-e02e6af183c8)|
|menu options                       | ![screen12](https://github.com/user-attachments/assets/576b0c96-c44f-4e90-86ae-31d83816c60c)|






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
