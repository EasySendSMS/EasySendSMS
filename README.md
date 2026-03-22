

# EasySendSMS — Bulk SMS API & Global SMS Gateway

**Send SMS Worldwide | HTTP & REST API | SMPP Gateway | HLR Lookup | Number Validation | 2-Way SMS**

[![Sign Up Free](https://img.shields.io/badge/Sign_Up-15_Free_SMS-brightgreen?style=for-the-badge)](https://my.easysendsms.app/register)
[![API Docs](https://img.shields.io/badge/Docs-Developer_Hub-blue?style=for-the-badge)](https://www.easysendsms.com/developers)
[![Coverage](https://img.shields.io/badge/Coverage-200%2B_Countries-orange?style=for-the-badge)](https://www.easysendsms.com/countries-list)



---

**[EasySendSMS](https://www.easysendsms.com)** is a global bulk SMS platform and SMS API gateway built for developers, businesses, and enterprises. Send OTP codes, transactional alerts, marketing campaigns, and two-way messages to over **200 countries** and **1,100+ mobile networks** — starting from just **$0.003 per SMS**.

Whether you need a simple HTTP API call to send a single message or an SMPP connection for high-throughput enterprise messaging, EasySendSMS provides the infrastructure, documentation, and support to get you live in minutes.

---

## API Endpoints

All API requests are made over HTTPS to `api.easysendsms.app`. The following endpoints are available:

| Endpoint | Base URL | Description |
| :--- | :--- | :--- |
| **Send SMS** | `https://api.easysendsms.app/bulksms` | Send single or bulk SMS (up to 30 numbers per request) |
| **Check Balance** | `https://api.easysendsms.app/balance` | Query your current account credit balance |
| **HLR Lookup** | `https://api.easysendsms.app/hlr` | Check live subscriber status, roaming, ported network |
| **Number Validation** | `https://api.easysendsms.app/nv` | Validate number format, country, operator, and type |

All endpoints support `GET` and `POST` methods. HTTPS is enforced for secure communication via SSL encryption.

> For full parameter references, response formats, error codes, and code examples, visit the [HTTP API Documentation](https://www.easysendsms.com/http-api) or the [REST API (v1) Documentation](https://www.easysendsms.com/developers).

---

## Quick Start — Send Your First SMS

Send an SMS in seconds using the HTTP API. Replace `your_username` and `your_password` with your [EasySendSMS account](https://my.easysendsms.app/register) credentials.

### cURL

```bash
curl -X POST https://api.easysendsms.app/bulksms \
  -d "username=your_username" \
  -d "password=your_password" \
  -d "to=12345678900" \
  -d "from=MyBrand" \
  -d "text=Hello%20from%20EasySendSMS" \
  -d "type=0"
```

### Python

```python
import http.client
import urllib.parse

params = urllib.parse.urlencode({
    'username': 'your_username',
    'password': 'your_password',
    'to': '12345678900',
    'from': 'MyBrand',
    'text': 'Hello from EasySendSMS',
    'type': '0'
})

headers = {'Content-Type': 'application/x-www-form-urlencoded'}

conn = http.client.HTTPSConnection("api.easysendsms.app")
conn.request("POST", "/bulksms", params, headers)
res = conn.getresponse()
print(res.read().decode("utf-8"))
```

### PHP

```php
$curl = curl_init();

curl_setopt_array($curl, array(
    CURLOPT_URL => 'https://api.easysendsms.app/bulksms',
    CURLOPT_RETURNTRANSFER => true,
    CURLOPT_CUSTOMREQUEST => 'POST',
    CURLOPT_POSTFIELDS => 'username=your_username&password=your_password&to=12345678900&from=MyBrand&text=Hello%20from%20EasySendSMS&type=0',
    CURLOPT_HTTPHEADER => array('Content-Type: application/x-www-form-urlencoded'),
));

$response = curl_exec($curl);
curl_close($curl);
echo $response;
```

**Successful Response:**
```
OK: 760d54eb-3a82-405c-a7a7-0a0096833615
```

> More code examples in **C#**, **Java**, **Node.js**, and other languages are available in the [Developer Hub](https://www.easysendsms.com/developers).

---

## Integration Methods

EasySendSMS supports multiple integration protocols to fit any architecture:

| Method | Best For | Documentation |
| :--- | :--- | :--- |
| **HTTP(S) API** | Simple integrations, web apps, scripts | [HTTP API Docs](https://www.easysendsms.com/http-api) |
| **REST API (v1)** | Modern applications, token-based auth | [REST API Docs](https://www.easysendsms.com/developers) |
| **SMPP v3.4** | High-throughput enterprise, aggregators | [SMPP Docs](https://www.easysendsms.com/developers) |
| **Webhook (DLR)** | Real-time delivery receipt callbacks | [Webhook Docs](https://www.easysendsms.com/developers) |
| **WordPress Plugin** | WordPress-based websites and stores | [WordPress Integration](https://www.easysendsms.com/developers) |

---

## Platform Features

### Bulk SMS Gateway

Send hundreds to millions of SMS messages globally with a single request. Our intelligent routing engine delivers messages with high speed and high deliverability across **200+ countries and 1,100+ mobile networks**. Set custom sender names, schedule messages, and track delivery in real time.

### OTP & Transactional SMS

Priority routing ensures time-sensitive messages like one-time passwords (OTP), two-factor authentication (2FA) codes, order confirmations, and system alerts are delivered instantly. Our infrastructure is optimized for low-latency, high-reliability delivery.

### HLR Lookup

Verify the live status of any mobile number before sending. Our [HLR Lookup](https://www.easysendsms.com/hlr-lookup) API returns subscriber status, roaming information, ported network data, MCC/MNC codes, and more. Clean your contact lists, reduce failed deliveries, and save on messaging costs.

### Number Validation

Our [Number Validation](https://www.easysendsms.com/number-validation) service checks whether a phone number is correctly formatted, identifies the country and original network, and determines if it is a mobile or landline number. Validate up to 30 numbers per request.

### Virtual Numbers & 2-Way SMS

Rent dedicated virtual numbers to send and receive SMS. Enable two-way conversations with your customers for support, feedback, interactive campaigns, and opt-out management.

### Webhook Delivery Receipts (DLR)

Receive real-time delivery status callbacks pushed directly to your server. Track message states (Delivered, Expired, Undelivered) and integrate delivery data into your CRM, analytics, or billing systems.

---

## Developer Resources

| Resource | Link |
| :--- | :--- |
| **Developer Hub** | [easysendsms.com/developers](https://www.easysendsms.com/developers) |
| **HTTP API Reference** | [easysendsms.com/http-api](https://www.easysendsms.com/http-api) |
| **GitHub SDKs & Examples** | [GitHub Repository](https://github.com/easysendsms) |
| **RapidAPI Integration** | [EasySendSMS on RapidAPI](https://www.easysendsms.com/developers) |
| **SMS Character Counter** | [Character Counter Tool](https://www.easysendsms.com/developers) |
| **Help Center** | [KnowledgeBase & Guides](https://www.easysendsms.com/developers) |

---

## SMS API Error Codes

The following error codes apply to the Send SMS HTTP API (`/bulksms`):

| Code | Description |
| :--- | :--- |
| **1001** | Invalid URL. One of the parameters was not provided or left blank. |
| **1002** | Invalid username or password parameter. |
| **1003** | Invalid type parameter. |
| **1004** | Invalid message. |
| **1005** | Invalid mobile number. |
| **1006** | Invalid sender name. |
| **1007** | Insufficient credit. |
| **1008** | Internal error (do NOT re-submit the same message). |
| **1009** | Service not available (do NOT re-submit the same message). |

---

## Getting Started

1. **Create a free account** at [my.easysendsms.app/register](https://my.easysendsms.app/register) — you get **15 free SMS credits** instantly.
2. **Get your API credentials** from the account dashboard.
3. **Choose your integration method** — HTTP API, REST API, or SMPP.
4. **Send your first message** using the code examples above or in the [Developer Hub](https://www.easysendsms.com/developers).

---

## Support

Our support team is available **24/7** via multiple channels:

| Channel | Contact |
| :--- | :--- |
| **Email** | support@easysendsms.com |
| **WhatsApp** | +1 (213) 221-0324 |
| **Live Chat** | Available on [easysendsms.com](https://www.easysendsms.com) |
| **Support Ticket** | [Contact Us](https://www.easysendsms.com/contact-us) |

---

<div align="center">

**[Website](https://www.easysendsms.com)** · **[Developers](https://www.easysendsms.com/developers)** · **[Countries Coverage](https://www.easysendsms.com/countries-list)** · **[Contact Us](https://www.easysendsms.com/contact-us)**

*EasySendSMS Sdn. Bhd. — Empowering global connectivity since 2017.*

</div>
