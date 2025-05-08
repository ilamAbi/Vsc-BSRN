import socket

# Discovery Dienst läuft auf allen Interfaces, Port 5005 
UDP_IP = "0.0.0.0"
UDP_PORT = 5005

#                     AF_INET= IPv4 , SOCK_DGRAM = UDP (nicht TCP)
sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)

# Binde Socket an IP+ Port
sock.bind((UDP_IP, UDP_PORT))
print(f"Discovery-Dienst läuft auf Port {UDP_PORT}...")