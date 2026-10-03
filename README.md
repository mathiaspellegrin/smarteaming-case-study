# Smarteaming

Scheduling, shifts, invoicing and payroll for companies with shift-based teams. In production since 2020 at [smarteaming.com](https://smarteaming.com). I built it and I run it, through my company MBP Enterprises Ltd.

The code is private. This page explains what Smarteaming does and how it's built.

## What it does

Companies with shift-based teams were planning in spreadsheets and group chats. Then they typed the same data again for invoices and payroll. Smarteaming does all of it in one place: availability, schedules, shifts, invoices, payroll and Dimona declarations (the Belgian employment registration).

## My role

I'm the only engineer. I built the backend, the web app and the mobile apps, I run the servers, and I fix things when they break.

## How it's built

- **API:** Node.js and Express, on MySQL with hand-written SQL (no ORM). Socket.IO pushes schedule changes in real time, and scheduled jobs send reminders.
- **Web app:** React and TypeScript, in English, French and Dutch. It's a static build, hosted on Hostinger.
- **Mobile apps:** iOS and Android, built with React Native (Expo). They wrap the web app and add push notifications, file downloads and offline detection.
- **Hosting:** the API runs on a DigitalOcean server behind Nginx, managed with PM2.

## In production

- About ten client companies and a few hundred users.
- Multi-tenant, with payroll and social-security data that can't be wrong.
- The API server has rebooted three times since August 2023, each time for under two minutes.
- Operations are written down: a deployment runbook, a decision log and a list of known issues.

## More

I'm happy to walk through the architecture in an interview.

- Portfolio: [mbp-enterprises.com](https://mbp-enterprises.com/work)
- LinkedIn: [Mathias Pellegrin](https://www.linkedin.com/in/mathiasp-793332239/)
- Email: mathias.pellegrin.pro@gmail.com
