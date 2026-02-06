# Warbixinta Mashruuca (Project Documentation)

Mashruucan waa **Starline Travel Application**, kaas oo loogu talagalay in lagu keydiyo, laguna maamulo duulimaadyada iyo tikidhada macaamiisha. Mashruucan wuxuu ka kooban yahay labo qaybood oo kala ah **Frontend** (Flutter) iyo **Backend** (Node.js & MongoDB).

## 1. Qaab Dhismeedka (Architecture)

Mashruucan wuxuu isticmaalayaa qaab dhismeedka **MVVM (Model-View-ViewModel)** si loo kala saaro qaybaha kala duwan ee koodka.

### MVVM Layers:

1.  **Model**: Waa qaybta mataleysa xogta (Data). Tusaale ahaan, `Flight` model oo qeexaya sida xogta duulimaadka u qaabaysan tahay (`id`, `airline`, `price`, iwm).
2.  **View**: Waa qaybta uu arko isticmaalaha (User Interface). Tusaale ahaan, `FlightsScreen` ama `BookingScreen`. Qaybtan ma qabanayso shaqo culus (logic), kaliya waxay soo bandhigtaa xogta.
3.  **ViewModel**: Waa buundada u dhaxaysa Model-ka iyo View-ga. Tusaale ahaan, `FlightViewModel`. Waxay maamushaa **State Management** (iyadoo la isticmaalayo `Provider`). Waxay xogta ka soo qaadaa Backend-ka, waxayna u gudbisaa View-ga si loo soo bandhigo.

### Faa'iidooyinka MVVM:

- Kala saarida UI-ga iyo Logic-ga (Separation of concerns).
- Koodka waa sahlan tahay in la dayactiro (Maintainability).
- Waa sahlan tahay in la tijaabiyo (Testability).

## 2. Backend Integration

Backend-ka wuxuu ku dhisanyahay **Node.js** iyo **Express**, xogtana waxaa lagu keydiyaa **MongoDB**.

- **API Routes**: Waxaan isticmaalnay REST API (`GET`, `POST`, `PUT`, `DELETE`).
- **Authentication**: Waxaan isticmaalnay **JWT (JSON Web Token)** si loo hubiyo amniga isticmaalaha.
- **Security**: Password-yada waa la sirqariyay (Hashed) ka hor inta aan la keydin (Bcrypt).

### API Endpoints List

#### 1. Users (Auth)

- `POST /api/users` - Register new user
- `POST /api/users/login` - Login user
- `GET /api/users/profile` - Get user profile (Protected)
- `PUT /api/users/profile` - Update user profile (Protected)

#### 2. Flights

- `GET /api/flights` - Get all flights
- `POST /api/flights` - Create flight (Admin only)
- `PUT /api/flights/:id` - Update flight (Admin only)
- `DELETE /api/flights/:id` - Delete flight (Admin only)

#### 3. Bookings

- `POST /api/bookings` - Create booking
- `GET /api/bookings/my` - Get my bookings
- `GET /api/bookings` - Get all bookings (Admin only)
- `PUT /api/bookings/:id/status` - Approve/Reject booking (Admin only)

#### 4. Messages

- `POST /api/messages` - Send message to admin
- `GET /api/messages` - Get all messages (Admin only)
- `POST /api/messages/:id/reply` - Reply to message (Admin only)

## 3. State Management

Waxaan isticmaalnay **Provider** package si aan u maamulno xaaladaha (states) application-ka.

- `ChangeNotifier`: Waxaa la isticmaalay si loo ogeysiiyo UI-ga marka xogta isbedesho (tusaale: marka duulimaad cusub lagu daro).
- `Consumer`: Waxaa la isticmaalay si loo dhageysto isbedelada oo kaliya qaybtaas loo cusbooneysiiyo (Rebuild).

## 4. Requirement Checklist Status

✅ **GitHub Repo**: Uploaded.
✅ **State Management**: Provider used correctly.
✅ **Architecture**: MVVM implemented and explained.
✅ **Backend Integration**: Node.js & MongoDB connected with real CRUD operations.
✅ **App Logo**: Custom logo configured.
✅ **Documentation**: Code fully commented in Somali language.
✅ **UI/UX**: Clean, professional design with consistent colors.
