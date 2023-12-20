import twilio
import twilio.rest
from twilio.rest import Client

account_sid = 'AC192171e5ee4384039b78ca249effcfd2'
auth_token = 'aac394d3256ef4dc3131fc19433e9b1e'
twilio_phone_number = '+12058596840'
recipient_number = '+916393193541'  # Replace with the recipient's phone number

# Initialize Twilio client
client = Client(account_sid, auth_token)
# Send a message with user's speech input and location link
location_link = 'https://maps.app.goo.gl/Uineoojq7LDxPGfJ6'  # Replace with the actual location URL
message_body = f'I am in need of help. Location: {location_link}'

message = client.messages.create(
    body=message_body,
    from_=twilio_phone_number,
    to=recipient_number
)

message = client.messages.create(
    from_='whatsapp:+14155238886',
    body=f'I am in need of help. Location: {location_link}',
    to='whatsapp:+919887551644'
)

emergency_contacts = ['+916393193541', '+919887551644','+916303082900']
message = client.messages.create(
    body=message_body,
    from_=twilio_phone_number,
    to=recipient_number
)
call = client.calls.create(
    url='http://demo.twilio.com/docs/voice.xml',
    to=recipient_number,
    from_=twilio_phone_number
)

for number in emergency_contacts:
    call = client.calls.create(
        url='http://demo.twilio.com/docs/voice.xml',
        to=number,
        from_=twilio_phone_number
    )

print(f"Call SID: {call.sid}")
print(f"Message SID: {message.sid}")
