# Getting Started with Commande cli


## Code of 'basic.py'
```python
import argparse

def main():
    parser = argparse.ArgumentParser(description="A simple command-line interface.")
    parser.add_argument("name", help="Your name")
    parser.add_argument("--age", type=int, help="Your age")
    parser.add_argument("--greet", action="store_true", help="Greet the user")
    
    args = parser.parse_args()

    if args.greet:
        if args.age:
            print(f"Hello, {args.name}! You are {args.age} years old.")
        else:
            print(f"Hello, {args.name}!")
    else:
        print("No action specified.")

if __name__ == "__main__":
    main()

```


## Run 
```bash
python cli_example.py John --age 30 --greet
```
## Result
```bash
Hello, John! You are 30 years old.
```
