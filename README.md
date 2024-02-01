import React from 'react';
import { BrowserRouter as Router, Route, Routes, Link } from 'react-router-dom';
import Home from './pages/Home';
import EmployeeList from './pages/EmployeeList';
import EmployeeDetails from './pages/EmployeeDetails';
import AddEmployee from './pages/AddEmployee';
import UpdateEmployee from './pages/UpdateEmployee';
import './Employee.css';

const App = () => {
    return ( <
        Router >
        <
        div > <
        div className = "navbar" >
        <
        Link to = "/" > Home < /Link> <
        Link to = "/employee-list" > Employee List < /Link> <
        Link to = "/add-employee" > Create Employee < /Link> < /
        div >

        { /* Routes */ } <
        Routes >
        <
        Route path = "/"
        element = { < Home / > }
        /> <
        Route path = "/employee-list"
        element = { < EmployeeList / > }
        /> <
        Route path = "/employee-details/:id"
        element = { < EmployeeDetails / > }
        /> <
        Route path = "/add-employee"
        element = { < AddEmployee / > }
        /> <
        Route path = "/update-employee/:id"
        element = { < UpdateEmployee / > }
        /> < /
        Routes > <
        /div> < /
        Router >
    );
};

export default App;
