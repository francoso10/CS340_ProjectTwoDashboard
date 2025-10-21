# CS340_ProjectTwoDashboard
## How do you write programs that are maintainable, readable, and adaptable?  
For this project, I focused on writing modular, well-documented code that could be reused and easily debugged.  
My `animal_shelter.py` CRUD module handled all MongoDB operations, which kept the dashboard (`ProjectTwoDashboard.ipynb`) focused only on user interaction and visualization logic.  
This structure followed the MVC pattern, MongoDB acted as the **Model**, and Dash served as both the **View** and **Controller**.  

Throughout development, I practiced defensive programming to make the dashboard more stable.  
When the DataTable crashed due to MongoDB’s `_id` ObjectID type, I fixed it by dropping that field before loading data into Pandas.  
When Dash callbacks threw a `NoneType object is not iterable` error, I added a simple condition to handle null column selections gracefully.  
These adjustments made the app more resilient and adaptable to future changes or different datasets.

---

## How do you approach a problem as a computer scientist?  
I approached the Grazioso Salvare dashboard as a set of smaller, testable goals connecting to the database first, then building the filters, and finally implementing charts and maps.  
Whenever I encountered an issue (like the CRUD import error or incorrect query results), I isolated the problem by testing small code blocks and reviewing MongoDB queries directly.  

This project required full-stack thinking: understanding both the backend data structure and the front-end behavior of Dash callbacks.  
Compared to earlier courses, this project emphasized iterative problem-solving and testing each component before moving on.  
Going forward, I’ll continue applying this incremental strategy to new projects to reduce complexity and improve reliability.

---

## What do computer scientists do, and why does it matter?  
Computer scientists design systems that transform data into actionable insights.  
In this case, the dashboard helps Grazioso Salvare identify rescue-dog candidates faster and more accurately using filters based on breed, age, and outcome data.  
Instead of manually scanning large CSV files, the user can now visualize the data interactively, saving time and improving decision-making.  

This project demonstrates how database systems, Python development, and UI design come together to solve real-world problems, showing that well-structured software can make organizations like Grazioso Salvare more efficient and data-driven.
