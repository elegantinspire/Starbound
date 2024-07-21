# Starbound

Starbound is a React and Django REST web application project designed to provide a modern, scalable, and efficient solution for a content website. 

## Features
**User Authentication**: Secure login and registration using JWT.
**Profile Management**: Users can update their profiles and view other users' profiles.
**Messaging System**: A chat application with real-time messaging.
**Updates**: Manage and display information.
**Help Center**: FAQs for assistance.
**Responsive Design**: Mobile-friendly layout for accessibility on all devices.

## Technical Stack

### Frontend

- **React**: For building a dynamic and responsive user interface.
- **Tailwind CSS**: For styling and ensuring a consistent design.
- **React Router**: For managing navigation and routing.

### Backend

- **Django**: For handling server-side logic and database interactions.
- **Django REST Framework**: For creating and managing API endpoints.
- **MySQL**: For a robust and scalable database solution.

### Project Structure

```plaintext
starbound/
├── backend/
│   ├── app/
│   ├── authentication/
│   ├── chatapp/
│   ├── profile/
│   └── systems
├── frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── context/
│       ├── helpers/
│       ├── layouts/
│       ├── pages/
│       ├── services/
│       ├── styles/
│       ├── types/
│       └── assets/
├── README.md
├── LICENSE
├── .gitattributes
├── .gitignore
```plaintext

##Getting Started

### Prerequisites

- Node.js and npm
- Python, pip and Django
- MySQL

### Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/elegantinspire/starbound.git
    cd starbound
    ```

2. **Frontend Setup**:

    ```bash
    cd frontend
    npm install
    npm start
    ```

3. **Backend Setup**:

    ```bash
    cd ../backend
    py -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install -r requirements.txt
    py manage.py migrate
    py load_initial_data.py # Populate Database with Sample data
    py manage.py runserver
    ```

4. **Database Configuration**:

    Update the `DATABASES` setting in `backend/starbound_backend/settings.py` to match your MySQL configuration:

    ```python
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'database_name',
            'USER': 'your_db_user',
            'PASSWORD': 'your_db_password',
            'HOST': 'localhost',
            'PORT': '3306',
        }
    }
    ```

5. **Environment Variables**:

    Create a `.env` file in the `backend` directory and add the necessary environment variables:

    ```env
    SECRET_KEY=your_secret_key
    DEBUG=True
    DATABASE_NAME=database_name
    DATABASE_USER=your_db_user
    DATABASE_PASSWORD=your_db_password
    DATABASE_HOST=localhost
    DATABASE_PORT=3306
    ```

## Usage

### Running the Development Servers

- **Frontend**: Navigate to the `frontend` directory and run:

    ```bash
    npm start
    ```

- **Backend**: Navigate to the `backend` directory and run:

    ```bash
    py manage.py runserver
    ```

The React frontend will be available at `http://localhost:3000`, and the Django backend will be available at `http://localhost:8000`.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Images: [Pexels](https://www.pexels.com/)
- Tools: [create-react-app](https://github.com/facebook/create-react-app), [Django](https://www.djangoproject.com/)

---

Starbound is designed to be a modern, scalable, and efficient solution for content websites. We welcome contributions and feedback from the community to improve and expand the project.
