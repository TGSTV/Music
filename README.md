import React, { useState, useEffect } from 'react';
import axios from 'axios';

const UserProfile = ({ userId }) => {
    const [user, setUser] = useState(null);

    useEffect(() => {
        const fetchUser = async () => {
            const response = await axios.get(`/api/users/${userId}`);
            setUser(response.data);
        };
        fetchUser();
    }, [userId]);

    if (!user) return <div>Loading...</div>;

    return (
        <div className="user-profile">
            <h1>{user.name}</h1>
            <p>{user.bio}</p>
            <h2>Portfolio</h2>
            <ul>
                {user.portfolio.map((item, index) => (
                    <li key={index}>{item}</li>
                ))}
            </ul>
            <h2>Reviews</h2>
            <ul>
                {user.reviews.map((review, index) => (
                    <li key={index}>{review}</li>
                ))}
            </ul>
        </div>
    );
};

export default UserProfile;
