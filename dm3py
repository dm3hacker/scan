import subprocess

def run_nikto(url):
    print("Running Nikto scan...")
    command = f"nikto -h {url}"
    process = subprocess.Popen(command.split(), stdout=subprocess.PIPE)
    output, error = process.communicate()
    if error:
        print(f"Nikto Error: {error}")
    else:
        print(output.decode())

def run_sqlmap(url):
    print("Running SQLMap scan...")
    command = f"sqlmap -u {url} --batch"
    process = subprocess.Popen(command.split(), stdout=subprocess.PIPE)
    output, error = process.communicate()
    if error:
        print(f"SQLMap Error: {error}")
    else:
        print(output.decode())

def run_xsstrike(url):
    print("Running XSStrike scan...")
    command = f"python3 XSStrike/xsstrike.py -u {url}"
    process = subprocess.Popen(command.split(), stdout=subprocess.PIPE)
    output, error = process.communicate()
    if error:
        print(f"XSStrike Error: {error}")
    else:
        print(output.decode())

def scan_website(url):
    run_nikto(url)
    run_sqlmap(url)
    run_xsstrike(url)

if __name__ == "__main__":
    url = input("Enter the URL of the website to scan: ")
    scan_website(url)

