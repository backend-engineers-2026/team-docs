# Week 2 Detailed Plan: Data Structures & File I/O

**Jan 26 - Feb 1, 2026**

---

## 🎯 Week Overview

This week bridges basic Python to real-world applications. You'll master Python's built-in data structures and file operations—foundational skills for backend development where you'll constantly manipulate data from databases, APIs, and configuration files.

---

## 📚 Learning Objectives

By end of week, you should be able to:

- Choose the right data structure for specific use cases
- Transform data efficiently using comprehensions
- Read/write files (text files only this week)
- Handle file operations safely with context managers
- Build practical CLI applications

---

## 🗓️ Daily Breakdown

### **DAY 1 (Mon, Jan 26): Lists & List Comprehensions**

**Theory (45 min):**

- List methods: append, extend, insert, remove, pop, sort
- List slicing and indexing
- List comprehensions vs loops (performance & readability)
- When to use lists vs other structures

**Practice (1.5 hours):**

```python
# Exercise 1: Student grade analyzer
grades = [85, 92, 78, 90, 88, 76, 95, 89]
# Tasks:
# - Find average
# - Get all grades above 85
# - Count failing grades (< 70)
# - Use comprehension to add 5 bonus points to all

# Exercise 2: List comprehension challenges
numbers = range(1, 51)
# - Get all even numbers
# - Get squares of odd numbers
# - Filter numbers divisible by both 3 and 5
```

**Build (45 min):**

```python
# Contact list manager (CLI)
# Features:
# - Add contact (name, phone)
# - Remove contact
# - Search by name
# - Display all sorted alphabetically
# Use list of dictionaries: [{"name": "John", "phone": "123"}]
```

**Key Takeaway:** Lists are for ordered, mutable sequences. Comprehensions make transformations concise.

---

### **DAY 2 (Tue, Jan 27): Dictionaries & Sets**

**Theory (45 min):**

- Dictionary operations: get, setdefault, update, pop
- Dict comprehensions
- Sets: unique elements, union, intersection, difference
- When to use dict vs list (O(1) lookup)

**Practice (1.5 hours):**

```python
# Exercise 1: Word frequency counter
text = "python is great python is powerful python is fun"
# Build dict: {"python": 3, "is": 3, ...}
# Find most common word

# Exercise 2: Student database
students = {
    "S001": {"name": "Alice", "grade": 85},
    "S002": {"name": "Bob", "grade": 92}
}
# - Add new student
# - Update grade
# - Find students with grade > 90
# - Use dict comprehension to create ID->name mapping

# Exercise 3: Set operations
team_a = {"Alice", "Bob", "Charlie"}
team_b = {"Bob", "Diana", "Eve"}
# Find: common members, all members, unique to team_a
```

**Build (45 min):**

```python
# Inventory management system
# Features:
# - Add item (name, quantity, price)
# - Update quantity (restock/sale)
# - Search item
# - Calculate total inventory value
# Use dict: {"laptop": {"qty": 10, "price": 1000}}
```

**Key Takeaway:** Dicts for key-value lookups (O(1)), sets for uniqueness and membership tests.

---

### **DAY 3 (Wed, Jan 28): Tuples & Advanced Data Structures**

**Theory (45 min):**

- Tuples: immutability, unpacking, use cases
- When to use tuple vs list
- Nested data structures (list of dicts, dict of lists)
- Combining data structures for complex problems

**Practice (1.5 hours):**

```python
# Exercise 1: Coordinate system
points = [(0, 0), (3, 4), (1, 2), (5, 12)]
# - Calculate distance from origin for each
# - Find point furthest from origin
# - Use tuple unpacking

# Exercise 2: Group students by grade
students = [
    ("Alice", "A"),
    ("Bob", "B"),
    ("Charlie", "A"),
    ("Diana", "C")
]
# Create dict to group: {"A": ["Alice", "Charlie"], ...}
# Count students per grade

# Exercise 3: Product catalog
# List of tuples: (product_id, name, price, category)
products = [
    (1, "Laptop", 999.99, "Electronics"),
    (2, "Desk", 199.99, "Furniture"),
    (3, "Mouse", 29.99, "Electronics")
]
# - Find all electronics
# - Calculate average price per category
# - Sort by price
```

**Build (45 min):**

```python
# Grade calculator with statistics
# Input: List of (student_name, score) tuples
# Output:
# - Class average
# - Letter grade distribution (A, B, C, D, F)
# - Top 3 students
# Use dictionaries to count grade distribution
```

**Key Takeaway:** Tuples for immutable data, combine data structures for real-world complexity.

---

### **DAY 4 (Thu, Jan 29): File I/O - Text Files**

**Theory (45 min):**

- File modes: r, w, a, r+, w+
- Context managers (`with` statement) - why they matter
- Reading: read(), readline(), readlines()
- Writing: write(), writelines()
- File paths and error handling basics

**Practice (1.5 hours):**

```python
# Exercise 1: Log file analyzer
# Create logs.txt with sample log entries
# Tasks:
# - Count total lines
# - Find lines with "ERROR"
# - Extract timestamps
# - Write errors to separate file

# Exercise 2: Configuration file
# Read config.txt:
# DATABASE_HOST=localhost
# DATABASE_PORT=5432
# Parse into dictionary using split('=')

# Exercise 3: File merger
# Combine multiple text files into one
# Add source filename as header for each section
```

**Build (45 min):**

```python
# Todo list with file persistence
# Features:
# - Add task (saves to todo.txt)
# - Mark complete (updates file)
# - List all tasks
# - Filter by status (pending/completed)
# File format: task_name|status
```

**Key Takeaway:** Always use context managers. Handle file operations safely. This is how you'll read configs in production.

---

### **DAY 5 (Fri, Jan 30): Advanced File Operations & Data Parsing**

**Theory (45 min):**

- Manual CSV parsing (splitting strings)
- Handling delimited data (comma, pipe, tab)
- String methods: split(), strip(), join()
- Multi-line file formats
- Data validation when reading files

**Practice (1.5 hours):**

```python
# Exercise 1: Manual CSV parsing
# Create students.txt:
# name,grade,age
# Alice,85,20
# Bob,92,21

# Read and parse:
with open('students.txt', 'r') as f:
    lines = f.readlines()
    
# Skip header, parse data
# Tasks:
# - Split each line by comma
# - Convert grade to int
# - Calculate average grade
# - Find students with grade > 85

# Exercise 2: Pipe-delimited data
# Create tasks.txt:
# task_name|status|priority
# Buy groceries|pending|high
# Write code|complete|medium

# Parse and display in organized format

# Exercise 3: Configuration file parser
# Create config.txt:
# DATABASE_HOST=localhost
# DATABASE_PORT=5432
# DATABASE_NAME=myapp

# Read and create dictionary:
# {"DATABASE_HOST": "localhost", ...}
# Use split('=') to parse key-value pairs
```

**Build (45 min):**

```python
# Expense tracker (Text file backend)
# File format: expenses.txt
# date|category|amount|description
# 2026-01-15|food|25.50|Lunch at cafe
# 2026-01-16|transport|10.00|Bus fare

# Features:
# - Add expense (append to file)
# - View all expenses
# - Filter by category
# - Calculate total by category
# - Monthly total

# Functions to create:
def add_expense(date, category, amount, description):
    # Format: date|category|amount|description
    # Append to file
    pass

def read_expenses():
    # Read file, parse each line
    # Return list of dicts
    pass

def filter_by_category(category):
    # Read all, filter matching category
    pass

def calculate_total():
    # Sum all amounts
    pass
```

**Key Takeaway:** You can parse structured data manually using string methods. This prepares you for working with CSV/JSON later.

---

### **DAY 6 (Sat, Jan 31): Team Session - Phone Book Project**

**Team Coding Session (2 PM-5 PM):**

Build a complete CLI phone book application together.

**Requirements:**

```python
# Phone Book Manager
# Storage: phonebook.txt
# Format: id|name|phone|email|category
# Example:
# 1|John Doe|1234567890|john@example.com|work
# 2|Jane Smith|0987654321|jane@example.com|personal

# Features:
# 1. Add contact
# 2. Search by name
# 3. Search by category (work, personal, family)
# 4. Update contact
# 5. Delete contact
# 6. List all contacts (sorted by name)
# 7. Statistics (total contacts, count by category)

# Core functions needed:
def generate_id():
    # Read file, find max id, return max+1
    pass

def add_contact(name, phone, email, category):
    # Generate id, format line, append to file
    pass

def read_contacts():
    # Read file, parse into list of dicts
    # [{"id": "1", "name": "John", ...}, ...]
    pass

def search_by_name(name):
    # Case-insensitive search
    pass

def update_contact(contact_id, field, new_value):
    # Read all, find by id, update field, rewrite file
    pass

def delete_contact(contact_id):
    # Read all, filter out matching id, rewrite file
    pass

def get_statistics():
    # Count total, count per category
    pass
```

**Session Structure:**

- **Hour 1:** Design file format & plan functions together
- **Hour 2:** Pair programming - implement core features
    - Pair 1: Add/Read functions
    - Pair 2: Search/Update functions
    - Pair 3: Delete/Statistics functions
- **Hour 3:** Integration, testing, code review, demo

**Learning Focus:**

- File-based CRUD operations (Create, Read, Update, Delete)
- Data validation (phone format, required fields)
- Error handling (file not found, invalid input)
- Reading entire file vs appending
- When to rewrite entire file (update/delete operations)

**Challenge Features (if time permits):**

- Duplicate phone number check
- Export contacts (formatted report)
- Backup file before updates

---

### **DAY 7 (Sun, Feb 1): Rest & Weekly Project**

**Individual Project (Optional, 2 hours):**

Build one of these to solidify the week's learning:

**Option 1: Grade Calculator System**

```python
# File: students.txt
# Format: student_id|name|subject|grade
# S001|Alice|Math|85
# S001|Alice|English|92
# S002|Bob|Math|78

# Features:
# - Add grade entry
# - Calculate student GPA (average of all subjects)
# - List all students with GPA
# - Find honor roll (GPA > 85)
# - Subject-wise statistics
```

**Option 2: Simple Inventory System**

```python
# File: inventory.txt
# Format: product_id|name|price|stock|category
# P001|Laptop|999.99|15|electronics
# P002|Desk|149.99|8|furniture

# Features:
# - Add product
# - Update stock (after sale/restock)
# - Low stock alerts (< 5 items)
# - Search by category
# - Calculate total inventory value
# - Sales recording (decrease stock)
```

**Option 3: Daily Journal**

```python
# File: journal.txt
# Format: date|mood|entry
# 2026-01-26|happy|Great day learning Python!

# Features:
# - Add journal entry (auto-date or manual)
# - View entries by date range
# - Search entries by keyword
# - Mood tracking (count happy/sad/neutral days)
# - Export specific month
```

---

## ✅ Weekly Deliverables

By Feb 1, each team member should have:

1. **5 Daily Exercises** (committed to GitHub)
    
    - Day 1: Contact list manager
    - Day 2: Inventory system
    - Day 3: Grade calculator with stats
    - Day 4: Todo list with persistence
    - Day 5: Expense tracker
2. **Phone Book Project** (team repo, Saturday session)
    
3. **1 Personal Project** (your choice from Day 7 options)
    
4. **Weekly Reflection** (Discord post):
    
    - What data structure do you understand best?
    - How did file I/O click for you?
    - What's still confusing?
    - How will you use this in backend?

---

## 🔗 Connection to Backend Development

**Why This Matters:**

|Skill|Backend Use Case|
|---|---|
|**Lists**|Processing query results from database|
|**Dicts**|JSON request/response bodies, config files|
|**Sets**|Removing duplicate user IDs, permissions checks|
|**Tuples**|Database row representation, immutable configs|
|**List Comp**|Transforming API responses efficiently|
|**File I/O**|Reading configs, writing logs|
|**Parsing**|Processing CSV imports, reading structured data|

**Real Example:**

```python
# FastAPI endpoint returning user data
@app.get("/users")
async def get_users():
    # Query returns list of tuples from PostgreSQL
    rows = await db.fetch("SELECT id, name, email FROM users")
    
    # Transform to list of dicts for JSON response
    users = [
        {"id": row[0], "name": row[1], "email": row[2]}
        for row in rows
    ]
    
    return {"users": users}  # FastAPI serializes dict to JSON
```

---

## 📖 Resources

**Official Docs:**

- [Python Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
- [Reading and Writing Files](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files)
- [String Methods](https://docs.python.org/3/library/stdtypes.html#string-methods)

**Practice:**

- [Practice Python](https://www.practicepython.org/)
- [Real Python - Working with Files](https://realpython.com/working-with-files-in-python/)

---

## 🎯 Success Criteria

You've mastered Week 2 if you can:

- [ ] Explain when to use list vs dict vs set vs tuple
- [ ] Write list comprehensions confidently
- [ ] Read/write text files safely with context managers
- [ ] Parse delimited data (comma, pipe, tab separated)
- [ ] Build a CLI app with file persistence
- [ ] Handle file operations properly
- [ ] Understand O(1) dict lookups vs O(n) list searches

---

## 💡 Pro Tips

1. **Always use context managers** for files - prevents resource leaks
    
    ```python
    with open('file.txt', 'r') as f:
        data = f.read()
    # File automatically closed
    ```
    
2. **Strip before splitting:**
    
    ```python
    line = "Alice,85,20\n"
    parts = line.strip().split(',')  # ['Alice', '85', '20']
    ```
    
3. **Validate data** before writing to files
    
4. **Use descriptive variable names** - `students` not `s`
    
5. **Test edge cases** - empty files, missing data, invalid formats
    

---

## 🚨 Common Mistakes to Avoid

1. **Forgetting to strip newlines:**
    
    ```python
    # Wrong:
    line.split(',')  # Last item has '\n'
    
    # Right:
    line.strip().split(',')
    ```
    
2. **Opening files without context manager:**
    
    ```python
    # Wrong:
    f = open('file.txt', 'r')
    data = f.read()
    # f.close() might never be called
    
    # Right:
    with open('file.txt', 'r') as f:
        data = f.read()
    ```
    
3. **Not converting string numbers:**
    
    ```python
    # Wrong:
    total = parts[2] + parts[3]  # String concatenation!
    
    # Right:
    total = int(parts[2]) + int(parts[3])
    ```
    

---

**Let's crush Week 2! 🚀**

This week you're building the foundation for data manipulation and persistence. Every backend application reads configs, processes data, and stores results. You're learning these fundamentals the right way.

**Monday standup format:**

```
📅 Date: Jan 27, 2026
✅ Yesterday: Completed Day 1 - Lists & comprehensions
🎯 Today: Working on Day 2 - Dictionaries & Sets
🚧 Blockers: None / [describe if any]
💡 Learning: List comprehensions are way cleaner than loops!
```

**See you Monday! Drop questions in Discord anytime. 💬**
