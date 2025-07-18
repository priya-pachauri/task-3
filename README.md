import tkinter as tk
from tkinter import messagebox, filedialog

class ToDoListApp:
    def __init__(self, root):
        self.root = root
        self.root.title("To-Do List")
        self.root.geometry("400x500")
        self.root.configure(bg="#f5f5f5")

        self.tasks = []

        self.task_entry = tk.Entry(self.root, font=("Arial", 14), width=25)
        self.task_entry.pack(pady=10)

        self.add_button = tk.Button(self.root, text="Add Task", width=20, command=self.add_task)
        self.add_button.pack(pady=5)

        self.tasks_listbox = tk.Listbox(self.root, font=("Arial", 12), width=35, height=15, selectmode=tk.SINGLE)
        self.tasks_listbox.pack(pady=10)

        self.delete_button = tk.Button(self.root, text="Delete Task", width=20, command=self.delete_task)
        self.delete_button.pack(pady=5)

        self.save_button = tk.Button(sel
