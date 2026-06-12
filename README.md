<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Warintorn Pradit - Portfolio</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; max-width: 800px; margin: 0 auto; padding: 20px; background-color: #000000; }
        .header { text-align: center; margin-bottom: 30px; padding: 20px; background: white; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
        .header h1 { margin: 0; color: #2c3e50; }
        .header p { color: #666; font-size: 1.1em; }
        
        /* สไตล์ของเมนู Tab */
        .tab-container { background: white; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); overflow: hidden; }
        .tabs { display: flex; background-color: #eee; border-bottom: 1px solid #ddd; }
        .tab-button { background-color: inherit; border: none; outline: none; cursor: pointer; padding: 14px 20px; transition: 0.3s; font-size: 16px; font-weight: bold; color: #555; flex: 1; }
        .tab-button:hover { background-color: #ddd; }
        .tab-button.active { background-color: white; color: #0366d6; border-bottom: 3px solid #0366d6; }
        
        /* เนื้อหาใน Tab */
        .tab-content { display: none; padding: 20px; animation: fadeEffect 0.5s; }
        .tab-content.active { display: block; }
        @keyframes fadeEffect { from {opacity: 0;} to {opacity: 1;} }
        
        ul { padding-left: 20px; }
        li { margin-bottom: 10px; }
        .badge { background: #eee; padding: 3px 8px; border-radius: 4px; font-size: 0.85em; font-family: monospace; color: #d73a49; }
    </style>
</head>
<body>

    <div class="header">
        <h1>Warintorn Pradit</h1>
        <p>Data Engineer & Backend Developer</p>
        <p>Bangkok, Thailand | <a href="mailto:warintorn.pradit@gmail.com">warintorn.pradit@gmail.com</a></p>
    </div>

    <div class="tab-container">
        <div class="tabs">
            <button class="tab-button active" onclick="openTab(event, 'Database')">🗄️ Database & API</button>
            <button class="tab-button" onclick="openTab(event, 'Python')">🐍 Python Automation</button>
            <button class="tab-button" onclick="openTab(event, 'Analytics')">⚙️ Tools & Analytics</button>
        </div>

        <div id="Database" class="tab-content active">
            <h2>Database & System Architecture</h2>
            <ul>
                <li><b>Real Estate Platform (Office & Metro):</b> Designed and managed complex MySQL database architectures, including logic for 'Virtual Rooms' mapping.</li>
                <li><b>Backend API Development:</b> Built robust internal APIs using <span class="badge">FastAPI</span> to deliver precise database endpoints for the frontend team.</li>
                <li><b>Server Administration:</b> Managed Linux servers and automated database migrations and backups using <span class="badge">mysqldump</span>.</li>
            </ul>
        </div>

        <div id="Python" class="tab-content">
            <h2>Python & Data Pipelines</h2>
            <ul>
                <li><b>Automated Data Extraction:</b> Developed scripts configured with <span class="badge">Cron Jobs</span> to scrape and process data, drastically reducing manual tasks.</li>
                <li><b>API Integrations:</b> Connected external services (Google Drive, Analytics, Sheets API) to build real-time data cleaning pipelines.</li>
                <li><b>Image Processing System:</b> Engineered automated bulk image resizing and categorization workflows using <span class="badge">Pillow</span> and <span class="badge">Wand</span>.</li>
            </ul>
        </div>

        <div id="Analytics" class="tab-content">
            <h2>Internal Tools & Web Analytics</h2>
            <ul>
                <li><b>Automated Leave System:</b> Developed an internal HR application using <span class="badge">AppSheet</span> and <span class="badge">Google Apps Script</span> with complex approval workflows.</li>
                <li><b>Tracking Implementation:</b> Managed the deployment of <span class="badge">Google Tag Manager (GTM)</span> and <span class="badge">GA4</span> to monitor in-depth user metrics.</li>
                <li><b>Interactive Dashboards:</b> Designed real-time dashboards connecting multiple data sources to drive executive decision-making.</li>
            </ul>
        </div>
    </div>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks;
            tabcontent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
                tabcontent[i].classList.remove("active");
            }
            tablinks = document.getElementsByClassName("tab-button");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].classList.remove("active");
            }
            document.getElementById(tabName).style.display = "block";
            document.getElementById(tabName).classList.add("active");
            evt.currentTarget.classList.add("active");
        }
    </script>

</body>
</html>
