# Digital-Life-Simulator
RUST
use std::io;

struct Student {
    roll_no: i32,
    name: String,
    marks: f32,
}

fn read_input() -> String {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    input.trim().to_string()
}

fn main() {
    let mut students: Vec<Student> = Vec::new();

    loop {
        println!("\n===== STUDENT MANAGEMENT SYSTEM =====");
        println!("1. Add Student");
        println!("2. View All Students");
        println!("3. Search Student by Roll No");
        println!("4. Exit");
        println!("Enter your choice:");

        let choice: i32 = read_input().parse().unwrap_or(0);

        match choice {
            1 => {
                println!("Enter Roll Number:");
                let roll_no: i32 = read_input().parse().unwrap();

                println!("Enter Name:");
                let name = read_input();

                println!("Enter Marks:");
                let marks: f32 = read_input().parse().unwrap();

                students.push(Student {
                    roll_no,
                    name,
                    marks,
                });

                println!("✅ Student added successfully!");
            }

            2 => {
                if students.is_empty() {
                    println!("⚠️ No students found.");
                } else {
                    println!("\n--- Student List ---");
                    for s in &students {
                        println!(
                            "Roll No: {} | Name: {} | Marks: {}",
                            s.roll_no, s.name, s.marks
                        );
                    }
                }
            }

            3 => {
                println!("Enter Roll Number to search:");
                let search_roll: i32 = read_input().parse().unwrap();
                let mut found = false;

                for s in &students {
                    if s.roll_no == search_roll {
                        println!(
                            "✅ Found: Roll No: {} | Name


#OUTPUT
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9e9a9808-76a4-411d-ab5c-87c9f04fbdf7" />


