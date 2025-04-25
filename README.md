# SeasonNotifier

**SeasonNotifier** is a web and mobile application designed to notify businesses about upcoming seasonal events, helping them optimize inventory, sales strategies, and marketing efforts. The application focuses on seasonal events, festivals, and holidays specific to Kerala, such as **Onam**, **Vishu**, **Eid**, **Christmas**, and many more.

---

## Project Overview

Retailers, especially in regions like Kerala, face challenges in preparing for seasonal demand due to a lack of timely insights. **SeasonNotifier** helps solve this by sending timely notifications and recommendations about upcoming seasonal events, allowing businesses to prepare in advance and capitalize on demand spikes.

---

## Features

- **Event Notifications**: Get notified about upcoming seasonal events based on location (Kerala) and business type.
- **Dynamic Event Dates**: Supports both fixed-date (e.g., Christmas, Kerala Piravi) and dynamic events (e.g., Onam, Eid) calculated via lunar/regional calendars.
- **Business Recommendations**: Get suggestions on what products or services to focus on during specific seasons.
- **Push Notifications**: Receive real-time alerts on events through web or mobile notifications.

---

## Key Events Supported

The application will support regional and global events, including:

- **Onam**
- **Vishu**
- **Eid ul-Fitr** and **Eid ul-Adha**
- **Christmas**
- **Kerala Piravi**
- **School Reopenings**
- **Summer Vacation**
- **Wedding Season (Housewarmings)**
- **Local festivals** (e.g., Thrissur Pooram, Navaratri)

---

## Tech Stack

- **Frontend**: React.js (PWA), React Native (for mobile app)
- **Backend**: Node.js with Express
- **Database**: MongoDB or PostgreSQL
- **APIs**:
  - **Aladhan API** for Islamic (Hijri) calendar events.
  - Custom lunar/regional calendar calculations for Onam, Vishu, and other Malayalam-based events.
  - Google Calendar API for holidays and school breaks.
- **Push Notifications**: Firebase Cloud Messaging
- **Deployment**: Heroku (Backend), Vercel/Netlify (Frontend)

---

## Installation

### Prerequisites

- Node.js (v16+)
- MongoDB (local or cloud-based like MongoDB Atlas)
- Firebase account (for push notifications)
- API keys for external APIs (e.g., Aladhan, Google Calendar)

### Clone the Repository

```bash
git clone https://github.com/yourusername/season-notifier.git
cd season-notifier
```

### Install Dependencies

```
npm install
```

### Set Up Environment Variables

Create a `.env` file in the root directory and add your API keys and environment variables:

```
MONGO_URI=your_mongodb_uri
FIREBASE_API_KEY=your_firebase_api_key
ALADHAN_API_KEY=your_aladhan_api_key
```

### Running the Application

#### Backend (API Server)

To run the backend API server:

```
cd backendnpm
start
```


#### Frontend (PWA)

To run the frontend development server:

```
cd frontendnpm 
start
```


Open the app at [http://localhost:3000](vscode-file://vscode-app/c:/Users/muzam/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-sandbox/workbench/workbench.html).

---

## API Endpoints

### `GET /events`

Fetch a list of all events based on region, type, and date range.

 **Query Params** :

* `region` - The region for which events are queried (e.g., `kerala`).
* `from_date` - Start date for events (e.g., `2025-08-01`).
* `to_date` - End date for events (e.g., `2025-09-30`).

 **Example** :

**GET** **/events?region=kerala**&from_date**=**2025-08-01**&to_date**=**2025-09-30**

---

### `GET /events/today`

Fetch events happening today.

---

### `GET /events/lunar`

Fetch events based on lunar/regional calendars.

 **Example** :

```
GET /events/lunar?region=kerala&calendar_type=malayalam&year=2025
```

---

### `POST /events/recommendations`

Get product/service recommendations based on business type and upcoming events.

 **Example** :

```
POST /events/recommendations
{
  "region": "kerala",  
  "business_type": "clothing"
}
```


---

## Future Enhancements

* **Mobile App** : Develop a mobile version using React Native to support push notifications and on-the-go updates.
* **Business Dashboard** : A dedicated dashboard for businesses to track inventory, analyze seasonal trends, and plan promotions.
* **Machine Learning** : Implement predictive analytics to recommend seasonal products based on past trends.
* **User Feedback** : Add a feedback system to improve recommendations based on user input.

---

## License

This project is licensed under the MIT License - see the [LICENSE](vscode-file://vscode-app/c:/Users/muzam/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-sandbox/workbench/workbench.html) file for details.

---

## Acknowledgments

* **Aladhan API** for providing Islamic calendar support.
* **Google Calendar API** for holiday data.
* **Firebase** for real-time notifications.

---

## Contributing

Feel free to fork this repository and create pull requests to improve the project. Contributions are always welcome!

If you have any questions, feel free to reach out to me at `muzammilibrahim13@.com`.

---

**Happy coding!**
