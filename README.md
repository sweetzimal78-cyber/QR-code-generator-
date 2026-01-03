import qrcode

# Get UPI ID from user
upi_id = input("Enter your UPI ID: ")

# Create UPI URLs for different apps
phonepe_url = f"upi://pay?pa={upi_id}&pn=RecipientName&mc=1234"
paytm_url = f"upi://pay?pa={upi_id}&pn=RecipientName&mc=1234"
google_pay_url = f"upi://pay?pa={upi_id}&pn=RecipientName&mc=1234"

# Generate QR codes
phonepe_qr = qrcode.make(phonepe_url)
paytm_qr = qrcode.make(paytm_url)
google_pay_qr = qrcode.make(google_pay_url)

# Save QR codes as images
phonepe_qr.save("phonepe_qr.png")
paytm_qr.save("paytm_qr.png")
google_pay_qr.save("google_pay_qr.png")

# Show QR codes
phonepe_qr.show()
paytm_qr.show()
google_pay_qr.show()
