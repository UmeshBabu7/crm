# CRM - Customer Relationship Management System

A comprehensive Django-based Customer Relationship Management (CRM) application for managing leads, agents, and customer interactions. This system helps organizations track potential customers, assign leads to agents, manage follow-ups, and organize leads by categories.

## Features

- **Lead Management**: Create, read, update, and delete leads with detailed information
- **Agent Management**: Assign leads to agents and manage agent accounts
- **Category Management**: Organize leads into categories (New, Contacted, Converted, Unconverted)
- **Follow-up Tracking**: Add follow-up notes and files for each lead
- **User Authentication**: Secure signup, login, and password reset functionality
- **Dashboard**: Overview of leads and statistics
- **Multi-tenant Support**: Organization-based data isolation
- **Profile Pictures**: Upload and manage lead profile pictures
- **File Attachments**: Attach files to follow-ups
- **Responsive Design**: Modern UI built with Tailwind CSS

## Technologies Used

- **Backend**: Django
- **Database**: SQLite (development), PostgreSQL (production-ready)
- **Frontend**: HTML, Tailwind CSS, Crispy Forms
- **Static Files**: WhiteNoise
- **Image Processing**: Pillow


The application will be available at `http://127.0.0.1:8000/`

### Access Points

- **Landing Page**: `http://127.0.0.1:8000/`
- **Dashboard**: `http://127.0.0.1:8000/dashboard/`
- **Leads**: `http://127.0.0.1:8000/leads/`
- **Agents**: `http://127.0.0.1:8000/agents/`
- **Admin Panel**: `http://127.0.0.1:8000/admin/`

## Project Structure

```
crm/
├── crm/                  # Main project directory
│   ├── settings.py       # Django settings
│   ├── urls.py          # Main URL configuration
│   └── wsgi.py          # WSGI configuration
├── leads/                # Leads app
│   ├── models.py        # Lead, Category, FollowUp models
│   ├── views.py         # Lead views and logic
│   ├── forms.py         # Lead forms
│   ├── urls.py          # Lead URL patterns
│   └── templates/       # Lead templates
├── agents/               # Agents app
│   ├── models.py        # Agent model
│   ├── views.py         # Agent views
│   ├── forms.py         # Agent forms
│   └── templates/       # Agent templates
├── theme/               # Theme app (Tailwind CSS)
│   └── static_src/      # Tailwind source files
├── templates/           # Global templates
│   ├── base.html        # Base template
│   ├── dashboard.html   # Dashboard page
│   └── landing.html     # Landing page
├── static/              # Static files (CSS, JS, images)
├── db.sqlite3           # SQLite database
├── manage.py            # Django management script
└── requirements.txt     # Python dependencies
```

## Usage

### Creating Your First Account

1. Navigate to the signup page: `http://127.0.0.1:8000/signup/`
2. Fill in your details and create an account
3. Log in with your credentials

### Managing Leads

- **Create Lead**: Navigate to Leads → Create Lead
- **View Leads**: Access the leads list from the dashboard
- **Update Lead**: Click on a lead to view details and edit
- **Assign Agent**: Assign leads to agents from the lead detail page
- **Add Follow-up**: Add follow-up notes and files to track interactions
- **Update Category**: Change lead category to track progress

### Managing Agents

- **Create Agent**: Navigate to Agents → Create Agent
- **View Agents**: See all agents in your organization
- **Update/Delete**: Manage agent accounts as needed

### Managing Categories

- Create custom categories to organize your leads
- Default categories: New, Contacted, Converted, Unconverted

## Management Commands

The project includes custom management commands for adding sample data:

```bash
python manage.py add_sample_data
python manage.py create_leads
```

