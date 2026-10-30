<!doctype html>
<html lang="en">
<head>
    <link rel="icon" type="image/svg+xml" href="../favicon.svg">
    <meta charset="utf-8">
    <title>Ben Binh Tran - CV</title>
    <style>
        /* === REQUIRED CSS BOILERPLATE === */
        @page { size: A4; margin: 0; }
        *, *::before, *::after { box-sizing: border-box; }
        html, body { margin: 0; padding: 0; }
        html { background-color: #ffffff; }
        @media (prefers-color-scheme: dark) {
            html { background-color: #1f1f1f; }
        }
        body {
            padding: 24px 0;
            margin: 0 auto;
            max-width: 900px !important;
            border: none !important;
            background: transparent !important;
        }
        
        .no-print {
            text-align: center;
            font-size: 11px;
            color: #666;
            margin-bottom: 10px;
        }

        .page {
            height: 297mm;
            margin: 0 auto 12px auto;
            padding: 12mm 16mm 10mm 16mm;
            background-color: #ffffff;
            border: 1px solid rgba(0, 0, 0, 0.12);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            position: relative;
            overflow: hidden;
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            font-size: 10pt; 
            line-height: 1.4;
            color: #334155;
        }
        @media screen and (max-width: 600px) {
            body { padding: 16px 0; }
            .page { margin: 0 auto 8px auto; border: none; padding: 12px 20px; height: auto; }
        }
        .page-content {
            flex: 1 1 0;
            min-height: 0;
            overflow: hidden;
        }
        .page-footer {
            flex-shrink: 0;
            margin-top: auto;
            padding-top: 4mm;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 8.5pt;
            color: #64748b;
        }
        
        @media print {
            *, *::before, *::after {
                box-shadow: none !important;
                text-shadow: none !important;
                -webkit-print-color-adjust: exact;
                print-color-adjust: exact;
            }
            .no-print {
                display: none !important;
            }
            body { 
                padding: 0 !important; 
                margin: 0 !important; 
                background: none; 
            }
            .page {
                margin: 0 !important;
                border: none !important;
                height: 100vh !important;
                max-height: 296mm !important;
                page-break-after: avoid !important;
                break-after: avoid !important;
                padding: 10mm 14mm 8mm 14mm !important;
            }
        }
        [contenteditable]:focus { outline: none; }

        /* === DOCUMENT SPECIFIC STYLES === */
        .cv-layout {
            display: flex;
            gap: 16px; 
            height: 100%;
        }

        .cv-sidebar {
            flex: 0 0 200px; 
            background-color: #1e293b;
            color: #f8fafc;
            padding: 16px;
            border-radius: 8px;
            display: flex;
            flex-direction: column;
            gap: 14px; 
        }

        .photo-container {
            text-align: center;
        }

        .profile-photo {
            width: 100px; 
            height: 100px;
            object-fit: cover;
            border-radius: 50%;
            border: 2px solid #94a3b8;
            margin: 0 auto;
            display: block;
        }

        .sidebar-header {
            text-align: center;
            margin-top: 4px;
        }

        .sidebar-header h1 {
            font-size: 14pt;
            margin: 0 0 4px 0;
            color: #ffffff;
            line-height: 1.1;
            letter-spacing: 0.5px;
        }

        .sidebar-header .title {
            font-size: 8.5pt;
            color: #94a3b8;
            font-weight: 600;
        }

        .sidebar-section {
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        .sidebar-section h2 {
            font-size: 9.5pt;
            color: #38bdf8;
            margin: 0;
            padding-bottom: 3px;
            border-bottom: 1px solid #475569;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .sidebar-item {
            font-size: 8pt;
            line-height: 1.3;
            margin-bottom: 4px;
        }

        .sidebar-item strong {
            display: block;
            color: #e2e8f0;
            font-weight: 600;
            margin-bottom: 2px;
        }

        .sidebar-item p { margin: 0; color: #cbd5e1; }

        .contact-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .contact-list li {
            font-size: 8pt;
            margin-bottom: 4px;
            color: #cbd5e1;
            word-wrap: break-word;
        }
        
        .contact-list.bulleted li::before {
            content: "• ";
            color: #38bdf8;
        }

        .cv-main {
            flex: 1;
            display: flex;
            flex-direction: column;
            padding-top: 4px;
        }

        .cv-main > * + * {
            margin-top: 14px; 
        }

        .main-section h2 {
            font-size: 11.5pt;
            color: #0f172a;
            margin: 0 0 8px 0;
            padding-bottom: 3px;
            border-bottom: 2px solid #cbd5e1;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .main-section p {
            margin: 0;
            text-align: justify;
        }

        .experience-item {
            margin-bottom: 10px;
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 2px;
        }

        .experience-title {
            font-weight: bold;
            font-size: 10.5pt;
            color: #1e293b;
            margin: 0;
        }

        .experience-meta {
            font-size: 8.5pt;
            color: #64748b;
            font-weight: 600;
        }

        .experience-company {
            font-size: 9.5pt;
            color: #475569;
            margin-bottom: 4px;
            font-style: italic;
        }

        ul.bullet-list {
            margin: 0;
            padding-left: 18px;
        }

        ul.bullet-list li {
            margin-bottom: 3px;
        }

        .competencies-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .competency-card {
            background-color: #f8fafc;
            border: 1px solid #e2e8f0;
            padding: 8px 10px; 
            border-radius: 6px;
        }

        .competency-card h3 {
            margin: 0 0 2px 0;
            font-size: 9.5pt;
            color: #0f172a;
        }
        
        .competency-card p {
            font-size: 8.5pt;
            margin: 0;
            color: #475569;
            line-height: 1.25;
        }

    </style>
</head>
<body>
    <div class="no-print">Print this document with the browser's A4 / default-scale settings and choose “Save as PDF”.</div>

    <div contenteditable="true">
        
        <section class="page">
            <div class="page-content">
                
                <div class="cv-layout">
                    <!-- Left Sidebar -->
                    <aside class="cv-sidebar">
                        
                        <div class="photo-container">
                            <!-- Change the image name to your actual photo file in the repo -->
                            <img src="BenTran.jpg" alt="Profile Photo" class="profile-photo">
                        </div>

                        <div class="sidebar-header">
                            <h1>BEN BINH TRAN</h1>
                            <div class="title">Planning & Engineering Agent (P&E)</div>
                        </div>

                        <div class="sidebar-section">
                            <h2>Contact Info</h2>
                            <ul class="contact-list">
                                <li><strong>Phone:</strong> +84 822 468 722</li>
                                <li><strong>Email:</strong> BenBinhTran@gmail.com</li>
                                <li><strong>Location:</strong> Ho Chi Minh City, Vietnam</li>
                                <li><strong>Portfolio:</strong> phoenixflix.vercel.app</li>
                                <li><strong>GitHub:</strong> github.com/PhoenixWeaver</li>
                            </ul>
                        </div>

                        <div class="sidebar-section">
                            <h2>Education</h2>
                            <div class="sidebar-item">
                                <strong>PhD Studies (Incomplete)</strong>
                                <p>Electrical & Computer Engineering<br>Brigham Young University<br>2010 – 2014</p>
                            </div>
                            <div class="sidebar-item">
                                <strong>MS, Electrical Engineering</strong>
                                <p>University of Arkansas<br>2008 – 2010</p>
                            </div>
                            <div class="sidebar-item">
                                <strong>BS, Electrical Engineering & Math</strong>
                                <p>University of Arkansas<br>2004 – 2008</p>
                            </div>
                        </div>

                        <div class="sidebar-section">
                            <h2>Skills & Tools</h2>
                            <ul class="contact-list bulleted">
                                <li>CEBS & ServiceNow</li>
                                <li>Excel Power Query & SQL</li>
                                <li>Power Automate & SharePoint</li>
                                <li>JavaScript, HTML/CSS, Node.js</li>
                                <li>RCA, SPC, SLA/KPI Tracking</li>
                            </ul>
                        </div>

                        <div class="sidebar-section">
                            <h2>Languages</h2>
                            <div class="sidebar-item">
                                <strong>English</strong>
                                <p>Professional (20 years U.S.)</p>
                            </div>
                            <div class="sidebar-item">
                                <strong>Vietnamese</strong>
                                <p>Native Proficiency</p>
                            </div>
                        </div>

                    </aside>

                    <!-- Right Main Content -->
                    <main class="cv-main">
                        
                        <div class="main-section">
                            <h2>Summary</h2>
                            <p>
                                Ph.D.-level Electrical and Computer Engineer who lived, studied, and worked in the United States for 20 years across academic research, manufacturing, retail, and service operations. Brings a strong foundation in Planning & Engineering support through First/Last Mile operations experience, SLA/KPI management, root-cause analysis, continuous improvement, and cross-functional coordination. Skilled in Excel/Power Query, SQL, CEBS, ServiceNow, SharePoint, and Power Automate.
                            </p>
                        </div>

                        <div class="main-section">
                            <h2>Core Competencies</h2>
                            <div class="competencies-grid">
                                <div class="competency-card">
                                    <h3>Planning & Engineering</h3>
                                    <p>First/Last Mile support, RPI monitoring, SLA recovery, SOP design, milestone handoffs.</p>
                                </div>
                                <div class="competency-card">
                                    <h3>Continuous Improvement</h3>
                                    <p>RCA, SPC, KPI dashboards, exception trending, process-improvement proposals.</p>
                                </div>
                                <div class="competency-card">
                                    <h3>Cross-Functional Coordination</h3>
                                    <p>Station, PUD, inbound clearance, and regional teams (China, Taiwan, Thailand, Malaysia).</p>
                                </div>
                                <div class="competency-card">
                                    <h3>Analytics & Automation</h3>
                                    <p>Excel/Power Query, Power BI basics, SQL, Power Automate, CEBS, ServiceNow, SharePoint.</p>
                                </div>
                            </div>
                        </div>

                        <div class="main-section">
                            <h2>Work Experience</h2>
                            
                            <div class="experience-item">
                                <div class="experience-header">
                                    <h3 class="experience-title">Customer Experience Agent (RPI Creator & Monitor)</h3>
                                    <span class="experience-meta">02/2026 – 08/2026</span>
                                </div>
                                <div class="experience-company">FedEx Vietnam | Ho Chi Minh City</div>
                                <ul class="bullet-list">
                                    <li>Created RPI C-MOD control numbers in CEBS and submitted SharePoint entries triggering bilingual consignee notifications.</li>
                                    <li>Monitored operational exception queues, flagged SLA risks, and escalated through management and regional RPI paths.</li>
                                    <li>Used Power Query, Excel, and SharePoint to track case aging, pickup-within-SLA percentages, and leading exception types.</li>
                                    <li>Implemented Power Automate flows to consolidate AWBs and automate HTML email notifications, reducing manual work.</li>
                                </ul>
                            </div>

                            <div class="experience-item">
                                <div class="experience-header">
                                    <h3 class="experience-title">Customer Service Partner Specialist</h3>
                                    <span class="experience-meta">2024 – 2025</span>
                                </div>
                                <div class="experience-company">Concentrix | Ho Chi Minh City</div>
                                <ul class="bullet-list">
                                    <li>Provided B2B platform support, technical triage, billing coordination, and high-priority dispute resolution.</li>
                                    <li>Escalated defects to engineering and logged root causes effectively in ServiceNow.</li>
                                </ul>
                            </div>
                            
                            <div class="experience-item">
                                <div class="experience-header">
                                    <h3 class="experience-title">Quality Control & Assurance Specialist</h3>
                                    <span class="experience-meta">2022 – 2023</span>
                                </div>
                                <div class="experience-company">Black Diamond & Kizik | USA</div>
                                <ul class="bullet-list">
                                    <li>Conducted statistical analysis (SPC) of test data to determine product and component strength ratings.</li>
                                    <li>Developed test fixtures for production monitoring and maintained quality record systems for product rating documents.</li>
                                </ul>
                            </div>

                        </div>

                        <div class="main-section">
                            <h2>Selected Projects & Automation</h2>
                            
                            <div class="experience-item">
                                <div class="experience-header">
                                    <h3 class="experience-title">Customer Experience Request Management Platform</h3>
                                    <span class="experience-meta">Power Automate, Power Apps, M365</span>
                                </div>
                                <ul class="bullet-list">
                                    <li>Multi-scenario workflow engine for AWB Label Requests, Clearance Requests, and operational exceptions with routing and SLA tracking.</li>
                                </ul>
                            </div>
                            
                            <div class="experience-item">
                                <div class="experience-header">
                                    <h3 class="experience-title">Unified Logistics Workflow - Bulk Booking Suite</h3>
                                    <span class="experience-meta">Vanilla JS, HTML/CSS, Regex</span>
                                </div>
                                <ul class="bullet-list">
                                    <li>Book Space Checker and Bulk Shipment Request tools with CED/eOPS parsing, weight/dimension checks, and Outlook-ready outputs.</li>
                                </ul>
                            </div>
                        </div>

                    </main>
                </div>

            </div>
            <footer class="page-footer">
                <span>Ben Binh Tran — Curriculum Vitae</span>
                <span>Page 1</span>
            </footer>
        </section>

    </div>
</body>
</html>