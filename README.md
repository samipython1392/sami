import tkinter as tk
from datetime import datetime
import time
import threading

def show_time():
    root = tk.Tk()
    root.title("ساعت")
    now = datetime.now().strftime("%H:%M:%S")
    label = tk.Label(root, text=f"ساعت رو یادت باشه: {now}", font=("Arial", 30))
    label.pack(padx=50, pady=50)
    root.mainloop()

def show_message():
    time.sleep(60) # انتخاب زمان (60) 
    msg = tk.Tk()
    msg.title("کارت دارم")
    label = tk.Label(msg, text="تا کی میخوای پشت سیستم بشینی ", font=("Arial", 30))
    label.pack(padx=50, pady=50)
    msg.mainloop()


threading.Thread(target=show_time).start()
threading.Thread(target=show_message).start()
یاد اور
