🚀 C++ AI-Powered Unit Test Generator
Welcome! This project is an AI-driven C++ unit test generator that harnesses the power of LLaMA3 (via Ollama) to create robust, automated Google Test cases for your C++ functions. Designed for simplicity and flexibility, it lets you focus on writing code while the AI helps you ensure correctness and coverage.

📦 Project Layout
text
cpp_test_generator/
│
├── functions.cpp        # Core function implementations
├── functions.h          # Function declarations
├── main.cpp             # Example usage and entry point
├── instructions.yaml    # YAML file: test rules and requirements
├── prompt.txt           # Input prompt for the LLM
├── README.md            # Project documentation (this file)
└── tests/
    └── test_main.cpp    # Google Test unit tests (AI-generated)
🤖 Workflow Overview
Develop Your Functions:
Write and declare your C++ logic in functions.cpp and functions.h.

Describe Test Requirements:
Specify your testing expectations and rules in instructions.yaml.

Prepare the AI Prompt:
Combine code and YAML into prompt.txt for the AI model.

Generate Tests with LLaMA3:
Use Ollama to run the LLM and generate Google Test code:

bash
ollama run llama3 < prompt.txt
Paste the output into tests/test_main.cpp.

Compile and Run Everything:

Build your main app:

bash
g++ -std=c++17 functions.cpp main.cpp -o app
./app
Build and run your tests:

bash
g++ -std=c++17 tests/test_main.cpp functions.cpp -lgtest -lgtest_main -pthread -o test_main
./test_main
🛠️ Setup & Requirements
C++17 or newer compiler (e.g., g++)

Google Test (gtest)

Install via package manager (sudo apt-get install libgtest-dev) or add locally

Ollama (for running LLaMA3)

LLaMA3 model (ollama pull llama3)

📝 Example Usage
Implement your logic in functions.cpp, declare in functions.h.

Add sample calls in main.cpp for demonstration.

Define test rules in instructions.yaml.

Prepare a prompt in prompt.txt for the AI.

Generate and copy test code into tests/test_main.cpp.

Compile and run both app and tests as shown above.

📋 Sample Table: Key Files & Roles
File	Purpose
functions.cpp/.h	Core logic and declarations
main.cpp	Program entry and usage examples
instructions.yaml	Test rules for the AI
prompt.txt	Input for LLaMA3 to generate tests
tests/test_main.cpp	Google Test cases (AI-generated)
⚡ Tips for Customization
Modify function names, logic, and comments to fit your coding style.

Expand instructions.yaml for more detailed or edge-case tests.

Add new features or functions to grow your project.

Use the AI to regenerate tests as your code evolves.

👤 Author
Harsh Ranjan
B.Tech CSE, KIIT University
GitHub: harshranjan2804