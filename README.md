import csv

def count_cybersecurity_rows(filename):
    count = 0

    with open(filename, 'r', newline='', encoding='utf-8') as file:
        reader = csv.reader(file)

        for row in reader:
            row_text = " ".join(row).lower()
            if "cybersecurity" in row_text:
                count += 1

    return count

# Example usage
result = count_cybersecurity_rows("data.csv")
print("Rows containing 'cybersecurity':", result)
