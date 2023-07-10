# goit-react-hw-07-phonebook

Built with Vite and deployed via GitHub Actions

<<<<< Phonebook - code refactoring to add backend using mockAPI.io >>>>>

Contact book
Performed refactoring of the Contact Book application code. Removed the code responsible for storing and reading contacts from the local storage, and add communication with the backend for storing contacts.

Backend
Created personal backend for development with the UI service mockapi.io. Created a resource contacts to get handpoint /contacts. Used resource constructor and described the contact object following the documentation.

State Form
Added the load and error indicator handling to the Redux state. To do this, changed the state form:

{
  contacts: {
    items: [],
    isLoading: false,
    error: null
  },
  filter: ""
}

Operations
Used createAsyncThunk to declare asynchronous action generators and make HTTP requests. Processed actions and changed data in Redux state with createSlice.

Declared the following operations:

fetchContacts - get an array of contacts (GET method) by GET request. The basic type of action "contacts/fetchAll".
addContact - add contact (POST method). Basic type of action "contacts/addContact".
deleteContact - deletes a contact (DELETE method). Basic type of action "contacts/deleteContact".
