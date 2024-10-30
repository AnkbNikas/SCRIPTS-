import subprocess

 

def discover_hosts(network_range):

    if not network_range:

        print("No network range provided.")

        return

 

    try:

        command = f'nmap -sn {network_range}'

        process = subprocess.Popen(command, shell=True, stdout=subprocess.PIPE, stderr=subprocess.PIPE)

        output, error = process.communicate()

       

        if process.returncode != 0:

            print("Error during the scan:")

            print(error.decode())

            return

       

        print("Discovered Hosts:\n")

        print(output.decode())

       

    except Exception as e:

        print(f"An error occurred: {e}")

 

if __name__ == "__main__":

    network_range = input("Enter the network range (e.g., 192.168.1.0/24): ")

    discover_hosts(network_range)
