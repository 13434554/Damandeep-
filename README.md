# Damandeep-# Damandeep Singh – LetsDefend Log Analysis
# ITECH1502 – Cybersecurity Fundamentals

import re
from collections import Counter
import matplotlib.pyplot as plt

# 1. Read logs from file
def read_logs(file_path):
    with open(file_path, 'r') as file:
        logs = file.readlines()
    return logs

# 2. Extract warning and error events
def extract_events(logs):
    events = []
    for log in logs:
        if "WARNING" in log or "ERROR" in log:
            events.append(log.strip())
    return events
