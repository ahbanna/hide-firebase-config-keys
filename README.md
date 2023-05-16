# Step: 1

Create a file named .env.local in your root folder (where package.json is
located)

# Step: 2 ((in .ebv.local file))

VITE_apiKey=put apiKey from firebase without "" 
VITE_authDomain=put authDomain from firebase without "" 
VITE_projectId=same 
VITE_storageBucket=same
VITE_messagingSenderId=same 
VITE_appId=same

## For example:

VITE_apiKey=AIzaSyB-jxMK53vKBWbOVorjH0LEXxHHDbWZTlw
VITE_authDomain=car-doctor-64b3f.firebaseapp.com VITE_projectId=car-doctor-64b3f
VITE_storageBucket=car-doctor-64b3f.appspot.com
VITE_messagingSenderId=188669985277
VITE_appId=1:188669985277:web:42fff7c6e7299a85421994

# Step: 3 (in firebase.config.js file)

const firebaseConfig = { 
  apiKey: import.meta.env.VITE_apiKey,
  authDomain: import.meta.env.VITE_authDomain, 
  projectId: import.meta.env.VITE_projectId, 
  storageBucket: import.meta.env.VITE_storageBucket,
  messagingSenderId: import.meta.env.VITE_messagingSenderId, 
  appId: import.meta.env.VITE_appId, 
  };
