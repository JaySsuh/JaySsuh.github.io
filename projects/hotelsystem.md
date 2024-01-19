---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Hotel Management"
date: 2024
published: true
labels:
  - computer programming
  - C++
summary: "It is a hotel management system, it is intended to create, manage, and book different types of rooms with different types of price points."
---

The goal of this project was to create a hotel management system, where we would create rooms with specific instructions such as, a room with A/C or no A/C, a room with a large or small bed, comfort of said room, and finally the daily rate that we as a hotel would charge the guest per day. We also had the option of adding more, or even deleting already existing rooms from the hotel itself. It's a simple, straightforward hotel managing system that anyone should be able to use.

Here is some code that illustrates the differnet types of options we are able to include in our hotel booking system:

```cpp
Room Room::addRoom(int rno) { //addRoom function for room details
    Room room;
    room.roomNumber = rno;
    std::cout << "\nType AC/Non-AC (A/N) : ";
    std::cin >> room.ac;
    std::cout << "\nType Comfort (S/N) : ";
    std::cin >> room.type;
    std::cout << "\nType Size (B/S) : ";
    std::cin >> room.stype;
    std::cout << "\nDaily Rent : ";
    std::cin >> room.rent;
    ++Room::count; //updates static count
    Room::rooms[Room::count - 1] = room; //adds new room to array
    std::cout << "\n Room Added Successfully!";
    return room;
}
