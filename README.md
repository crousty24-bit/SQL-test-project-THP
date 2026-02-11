# SQL Test Project - The Hacking Project

A comprehensive SQL learning and practice project featuring multiple database schemas and real-world use cases. This project demonstrates fundamental database design concepts through practical SQLite implementations.

## 📚 Project Overview

This repository contains a collection of SQL databases showcasing different application architectures and design patterns. Each database is built with SQLite and represents a distinct real-world scenario for learning and practicing SQL querying, schema design, and relational database concepts.

## 🗂️ Project Structure

```
SQL-test-project-THP/
├── db/                                    # SQLite database files
│   ├── moocademy.sqlite                   # Online learning platform
│   ├── hacking_pinterest.sqlite           # Image sharing social platform
│   ├── hacking_news.sqlite                # Link sharing & discussion forum
│   ├── hacking_class.sqlite               # Class management system
│   ├── blog.sqlite                        # Blogging platform
│   └── chinook.db                         # Sample music store database
├── Data Base concepts de sites.md         # Database schema documentation
├── ERD SQL db concepts.png                # Entity Relationship Diagram
└── README.md                              # This file
```

## 💾 Database Examples

### 1. **MOOCademy** - Online Learning Platform
A course management system featuring instructional content organization.

**Tables:**
- `course` - Course catalog with titles and descriptions
- `lesson` - Individual lessons linked to courses

**Use Case:** Learning structured content relationships and hierarchical data

### 2. **The Hacking Pinterest** - Image Sharing Platform
A social media application focused on image sharing and community interaction.

**Tables:**
- `users` - User profiles
- `pins` - Shared images with URLs
- `comments` - User comments on pins

**Use Case:** Understanding many-to-many relationships and user-generated content

### 3. **The Hacking News** - Link Sharing & Discussion Forum
A news aggregation platform with collaborative discussion features.

**Tables:**
- `hack_users` - User profiles
- `links` - Shared links
- `new_comments` - Discussion comments on links

**Use Case:** Practicing content curation systems and comment threading

### 4. **Additional Databases**
- **hacking_class.sqlite** - Class/student management system
- **blog.sqlite** - Blog platform with articles and comments
- **chinook.db** - Sample music retailer database (learning dataset)

## 📊 Schema Documentation

Detailed database schemas and entity relationships are documented in [Data Base concepts de sites.md](Data%20Base%20%20concepts%20de%20sites.md). An Entity Relationship Diagram (ERD) is available in [ERD SQL db concepts.png](ERD%20SQL%20db%20concepts.png).

## 🎯 Learning Objectives

This project helps you master:
- **Schema Design** - Creating well-organized database structures
- **Relationships** - One-to-many and many-to-many associations
- **SQL Queries** - SELECT, INSERT, UPDATE, DELETE operations
- **Data Integrity** - Foreign keys and relational constraints
- **Database Normalization** - Organizing data efficiently

## 🚀 Getting Started

### Prerequisites
- SQLite3 (or any SQL client supporting SQLite)
- Basic understanding of SQL concepts

### Accessing Databases

To open and query any database:

```bash
sqlite3 db/moocademy.sqlite
```

Or use a GUI tool like:
- **DBeaver** (free, cross-platform)
- **SQLiteStudio** (open-source)
- **DB Browser for SQLite** (lightweight)

## 📝 Usage Examples

Once connected to a database, you can run queries:

```sql
-- Example: View all courses in MOOCademy
SELECT * FROM cours;

-- Example: Find all pins with their user information
SELECT pins.id, pins.image, utilisateurs.nom 
FROM pins
JOIN utilisateurs ON pins.utilisateurs_id = utilisateurs.id;

-- Example: Count comments per link
SELECT liens_id, COUNT(*) as comment_count 
FROM commentaires
GROUP BY liens_id;
```

## 📖 Recommended Learning Path

1. Start with **MOOCademy** - Simple one-to-many relationships
2. Move to **The Hacking Pinterest** - User interactions and comments
3. Explore **The Hacking News** - Multi-table joins and aggregations
4. Practice with **blog.sqlite** and **hacking_class.sqlite** - Real-world scenarios
5. Use **chinook.db** - Practice with a complete commercial dataset

## 🔧 Key Concepts Covered

| Concept | Database | Notes |
|---------|----------|-------|
| One-to-Many | All | Parent-child relationships |
| Many-to-Many | Pinterest, News | Users interacting with content |
| Aggregation | All | COUNT, SUM, GROUP BY operations |
| Joins | All | INNER, LEFT, RIGHT joins |
| Foreign Keys | All | Maintaining referential integrity |

## 📌 Notes

- All databases use **SQLite** for lightweight, file-based storage
- Schema documentation is maintained in Markdown format
- Visual ERD diagram included for quick reference
- Suitable for beginners to intermediate SQL learners

## 🤝 Contributing

This is a learning project. Feel free to:
- Add sample data to practice INSERT operations
- Create views and triggers for advanced SQL practice
- Submit improvements to schema documentation

## 📄 License

This project is part of The Hacking Project learning curriculum.

---

**Last Updated:** February 2026

**Status:** Active Learning Project