# Programming_Robust_HW
#Programming - Robust Programming
'''Ask the user for 5 ages of secondary school students. 
They must be valid ages of students in year 7-13: 11 to 18 years old
Add them up, find the difference between the oldest and youngest'''

def get_age(prompt):
    while True:
        try:
            age = int(input(prompt))
            if 11 <= age <= 18:
                return age
            else:
                print("Please enter an age between 11 and 18.")
        except ValueError:
            print("Invalid input. Please enter a valid integer")
def main():
    ages = []
    print("Please enter the ages of 5 secondary school students:")
    for i in range(5):
        age = get_age(f" Age {i + 1}: ")
        ages.append(age)

    total_age = sum(ages)
    age_difference = max(ages) - min(ages)

    print(f"The total ages is {total_age}")
    print(f"The difference between the youngest and oldest is: {age_difference}")

if __name__ == "__main__":
    main()
