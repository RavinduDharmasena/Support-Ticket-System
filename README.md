Assumptions
•	Agents can assign pending tickets for themselves.
•	Only unassigned tickets are available in the pending tickets. All assigned tickets will be under a separate view called my tickets in admin panels.
•	Customer need to provide the reference number to see the status of the ticket.
•	After agent replying to the customer, the ticket will be closed.
•	After assigning the support ticket to the agent, until the agent start working on the support ticket, it will be in assigned state.
•	The ticket status is pending, assigned, in-progress, closed.
•	Agent and customer are using 2 separate interfaces to report support tickets.
•	Once a ticket has been assigned to an agent, it can’t reassign to another agent.
•	Once a ticket has been assigned to an agent, it can’t be unassigned as well.
•	Once the ticket has been assigned to a agent, only that agent can see that ticket.

Instructions
1.	Make sure PHP 8.4, composer (version 2.9.5), MySQL Server 9.3 and NodeJS 24.15 LTS are installed and should up and running. Internet connection also required.
2.	Place the project inside a server such as Laravel Herd, XAMPP etc. This was developed in Laravel Herd development environment.
3.	Run "npm install" command inside the project folder.
4.	Run "composer install" command inside the project folder.
5.  Make sure to copy the .env.example file and rename it as .env.
6.	Add necessary email and db configurations in the .env file accordingly to receive the mails and for the assurance of proper database operations. You can use mailtrap configurations in here since mailtrap has been used as the 3rd party mail service.
7.  Make sure to run the command "php artisan key:generate" to generate a key to the application.
8. Run "php artisan migrate" to create the database.
9. Make sure to run the command "npm run dev" inside the project folder, in a separate terminal to make sure the UIs are rendering properly.
10. Run command "php artisan db:seed" to generate sample data. This will create 2 sample agents and 10 sample tickets that are in open state.
11. Open the project in the browser and if you encounter any error, try hard refresh.
11. you can log in to agent admin panel using following credentials
    - Agent 1
        - Username: admin@support.com
        - Password: password
    - Agent 2
        - Username: agent@support.com
        - Password: password


Improvements
1. Used Laravel Flux for responsive UIs.
2. Used Laravel Livewire for dynamic page components to reduce the page refreshes.
3. Used Tailwind CSS as CSS framework. 

All the UI components are got from Laravel Flux library and modified as necessary. The links for those code snippets are given below.
1. https://fluxui.dev/layouts/sidebar
2. https://fluxui.dev/components/input
3. https://fluxui.dev/components/modal
4. https://fluxui.dev/components/navbar
5. https://fluxui.dev/components/textarea
6. https://fluxui.dev/components/field
7. https://fluxui.dev/components/icon
8. https://fluxui.dev/components/button
9. https://fluxui.dev/components/heading
10. https://fluxui.dev/components/switch
11. https://tailwindcss.com/plus/ui-blocks/marketing/sections/header

This project is based on Livewire Starter Kit. All the authentication related stuff and the basic dashboard layout including the UIs are implemented by the Livewire Starter Kit.




