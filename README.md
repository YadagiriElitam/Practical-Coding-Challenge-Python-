def get_top_student(student_list):
    if not student_list:
        return None
    top_student = max(
        student_list, 
        key=lambda s: sum(s["grades"]) / len(s["grades"])
    )
    
    return top_student
students = [
    {"name": "Alice", "grades": [85, 90, 78]},
    {"name": "Bob", "grades": [92, 88, 95]},
    {"name": "Charlie", "grades": [76, 82, 80]}
]

result = get_top_student(students)
print(f"The top student is {result['name']} with an average of {sum(result['grades'])/3:.2f}")
