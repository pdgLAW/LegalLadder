# LegalLadder
This project provides a visual representation of the Indian judiciary hierarchy. It provides a structured, easy-to-understand flowchart of the court system, from the Supreme Court to lower magistrate courts. It is perfect for law students, researchers, and legal professionals.
<!DOCTYPE html>
<!-- saved from url=(0060)file:///C:/Users/dasgu/OneDrive/Desktop/court_flowchart.html -->
<html lang="en"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Complete Indian Court Hierarchy</title>
    <style>
        :root {
            --supreme-court: #d32f2f;
            --high-court: #1976d2;
            --sessions: #388e3c;
            --cjm: #0097a7;
            --metro-magistrate: #7b1fa2;
            --jmfc: #f57c00;
            --jmsc: #afb42b;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background: #f0f0f0;
            line-height: 1.6;
        }

        .court-node {
            padding: 15px 25px;
            margin: 15px auto;
            width: 300px;
            border-radius: 8px;
            color: white;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            transition: transform 0.2s;
            text-align: center;
        }

        .court-node:hover {
            transform: scale(1.05);
        }

        .details-pane {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 30px;
            border-radius: 10px;
            width: 85%;
            max-width: 700px;
            max-height: 80vh;
            overflow-y: auto;
            z-index: 1000;
            box-shadow: 0 0 25px rgba(0,0,0,0.3);
        }

        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 999;
        }

        .close-btn {
            float: right;
            cursor: pointer;
            font-size: 24px;
            margin: -10px -10px 0 0;
        }

        .legal-ref {
            color: #d32f2f;
            font-weight: bold;
        }

        .section-heading {
            color: #1976d2;
            margin: 20px 0 10px;
            font-size: 1.1em;
        }
    </style>
</head>
<body>
    <h1 style="text-align: center">Complete Hierarchy of Criminal Courts in India</h1>

    <!-- Court Nodes -->
    <div class="court-node" style="background: var(--supreme-court)" onclick="showDetails(&#39;supreme&#39;)">
        Supreme Court of India
    </div>

    <div class="court-node" style="background: var(--high-court)" onclick="showDetails(&#39;high&#39;)">
        High Courts
    </div>

    <div class="court-node" style="background: var(--sessions)" onclick="showDetails(&#39;sessions&#39;)">
        Sessions Court
    </div>

    <div class="court-node" style="background: var(--cjm)" onclick="showDetails(&#39;cjm&#39;)">
        Chief Judicial Magistrate (CJM)
    </div>

    <div class="court-node" style="background: var(--metro-magistrate)" onclick="showDetails(&#39;metro&#39;)">
        Metropolitan Magistrates
    </div>

    <div class="court-node" style="background: var(--jmfc)" onclick="showDetails(&#39;jmfc&#39;)">
        JMFC
    </div>

    <div class="court-node" style="background: var(--jmsc)" onclick="showDetails(&#39;jmsc&#39;)">
        JMSC
    </div>

    <!-- Overlay and Details Pane -->
    <div class="overlay" id="overlay" onclick="closeDetails()" style="display: none;"></div>
    <div class="details-pane" id="detailsPane" style="display: none;">
        <span class="close-btn" onclick="closeDetails()">×</span>
        <div id="content">
                <h2>Metropolitan Magistrates</h2>
                
                    <p><span class="legal-ref">Established under:</span> Section 16 of the Code of Criminal Procedure (CrPC): This section mandates the establishment of Courts of Metropolitan Magistrates in every metropolitan area, defined as areas with a population exceeding one million.</p>
                    
                    <div class="section-heading">Jurisdiction:</div>
                    <p>Geographical Jurisdiction: The jurisdiction of a Metropolitan Magistrate extends throughout the metropolitan area, allowing them to try offenses committed within that territory.<br>
                    Types of Cases: They can handle a wide range of criminal cases, typically those punishable with imprisonment for a term not exceeding three years.</p>
                    
                    <div class="section-heading">Composition:</div>
                    <p>The presiding officers of these courts are appointed by the High Court. Each metropolitan area will have as many Metropolitan Magistrates as deemed necessary by the State Government in consultation with the High Court.</p>
                    
                    <div class="section-heading">Powers and Functions:</div>
                    <p>Trial Powers: A Metropolitan Magistrate has the powers of a first-class magistrate, which includes trying offenses punishable with imprisonment for up to three years and imposing fines not exceeding ₹10,000 (as per Section 29 of the CrPC).<br>
                    Administrative Role: They operate under the supervision of the Chief Metropolitan Magistrate and are subordinate to them. The Chief Metropolitan Magistrate has regulatory powers over their functions.<br>
                    Special Metropolitan Magistrates: Under Section 18 of the CrPC, Special Metropolitan Magistrates may be appointed with similar powers for specific cases or functions.</p>
                    
                    <div class="section-heading">Sentencing Powers:</div>
                    <p>A Metropolitan Magistrate can impose sentences consistent with those applicable to first-class magistrates, specifically for offenses punishable by up to three years in prison or fines up to ₹10,000.</p>
                    
                    <div class="section-heading">Summary</div>
                    <p>Metropolitan Magistrates serve an essential role in the criminal justice system within metropolitan areas, handling a variety of offenses while operating under the jurisdiction defined by the CrPC. They possess significant trial powers and are integral to maintaining law and order in urban settings. However, they do not have jurisdiction over cases involving more severe penalties, which are reserved for higher courts.</p>
                
            </div>
    </div>

    <script>
        const courtData = {
            supreme: {
                title: "Supreme Court of India",
                content: `
                    <p><span class="legal-ref">Established under:</span> Article 124 of the Constitution</p>
                    <div class="section-heading">Highest appellate authority:</div>
                    <p>The Supreme Court is the apex court in India, serving as the final court of appeal.</p>
                    
                    <div class="section-heading">Original jurisdiction:</div>
                    <p>It has original jurisdiction in disputes between states.</p>
                    
                    <div class="section-heading">Power to issue writs:</div>
                    <p>The Supreme Court can issue writs for the enforcement of fundamental rights under Article 32.</p>
                    
                    <div class="section-heading">Special Leave Petitions:</div>
                    <p>It can grant special leave to appeal from any judgment, decree, determination, sentence, or order in any cause or matter passed or made by any court or tribunal in India.</p>
                    
                    <div class="section-heading">Death sentence cases:</div>
                    <p>While the Supreme Court can hear appeals involving death sentences, it does not have a mandatory requirement to confirm them.</p>
                `
            },
            high: {
                title: "High Courts",
                content: `
                    <p><span class="legal-ref">Established under:</span> Article 214 of the Constitution</p>
                    
                    <div class="section-heading">Highest appellate jurisdiction:</div>
                    <p>The High Courts are the highest courts of appellate jurisdiction in each state and union territory of India.</p>
                    
                    <div class="section-heading">Original jurisdiction:</div>
                    <p>Some High Courts (Calcutta, Bombay, Madras, and Delhi) have original civil jurisdiction in cases of higher value.<br>
                    All High Courts have original jurisdiction in cases related to wills, divorce, contempt of court, and admiralty.<br>
                    Can hear disputes relating to the election of members of Parliament and State Legislatures.</p>
                    
                    <div class="section-heading">Writ jurisdiction:</div>
                    <p>Empowered to issue writs (habeas corpus, mandamus, certiorari, prohibition, and quo warranto) for the enforcement of fundamental rights and for any other purpose (i.e., enforcement of an ordinary legal right).<br>
                    Writ jurisdiction is concurrent with the Supreme Court, but the High Court's writ jurisdiction is wider, as it extends to the enforcement of fundamental rights and any ordinary legal right.</p>
                    
                    <div class="section-heading">Appellate jurisdiction:</div>
                    <p>In civil cases, appeals can be made to the High Court against a district court’s decision.<br>
                    In criminal cases, appellate jurisdiction extends to cases decided by Sessions and Additional Sessions Judges.</p>
                    
                    <div class="section-heading">Supervisory jurisdiction:</div>
                    <p>The High Court has superintendence over all courts and tribunals within its territorial jurisdiction, except military courts.<br>
                    This includes administrative as well as judicial superintendence.<br>
                    Can call for returns from subordinate courts and issue rules for regulating their practices.</p>
                    
                    <div class="section-heading">Power of Superintendence:</div>
                    <p>As per Article 227 of the Constitution of India, the High Court has superintendence over all Courts and Tribunals throughout the territory of India. The power of superintendence includes a revisional jurisdiction to intervene in cases of gross injustice or non-exercise or abuse of jurisdiction even though no appeal or revision against the order was available.</p>
                `
            },
            sessions: {
                title: "Sessions Court",
                content: `
                    <p><span class="legal-ref">Established under:</span><br>
                    Section 9 of the CrPC: The Court of Sessions is instituted in each sessions division by the State Government.<br>
                    Section 7 of the CrPC: Every state shall consist of sessions divisions, with each division serving as a district or consisting of districts.</p>
                    
                    <div class="section-heading">Composition:</div>
                    <p>The presiding officer is known as the Sessions Judge, appointed by the High Court under whose jurisdiction the sessions division falls. Additional Sessions Judges may also be appointed as needed.</p>
                    
                    <div class="section-heading">Jurisdiction:</div>
                    <p>Criminal Jurisdiction: The Sessions Court can try any offense under the Indian Penal Code (IPC) and has jurisdiction over offenses punishable with imprisonment for a term exceeding seven years (Section 28 of the CrPC).<br>
                    Territorial Jurisdiction: Determined by where the offense occurred.</p>
                    
                    <div class="section-heading">Powers and Functions:</div>
                    <p>Conducting Trials: The Sessions Court is responsible for conducting trials for serious criminal offenses, ensuring fair proceedings and delivering judgments based on evidence presented by both prosecution and defense.<br>
                    Appellate Jurisdiction: Acts as an appellate court, hearing appeals from judgments passed by Magistrates within its jurisdiction.<br>
                    Revisional Powers: Under Section 397 of the CrPC, a Sessions Judge may exercise powers similar to those of the High Court in revising decisions made by lower courts.<br>
                    Special Jurisdictions: May act as a Special Judge under various acts, such as the Scheduled Caste/Scheduled Tribes (Prevention of Atrocities) Act and the Prevention of Corruption Act.</p>
                    
                    <div class="section-heading">Sentencing Powers:</div>
                    <p>The Sessions Court can impose a full range of penalties for criminal acts, including life imprisonment and the death penalty. However, any death sentence passed must be confirmed by the High Court (Section 28 of the CrPC).</p>
                    
                    <div class="section-heading">Summary</div>
                    <p>The Sessions Court plays a crucial role in India's criminal justice system, handling serious offenses, conducting trials, and serving as an appellate body for lower courts. It has significant powers to ensure justice while maintaining checks and balances through its revisional authority.</p>
                `
            },
            cjm: {
                title: "Chief Judicial Magistrate (CJM)",
                content: `
                    <p><span class="legal-ref">Established under:</span> Section 12 of the CrPC: The Chief Judicial Magistrate is appointed by the High Court in every district (not being a metropolitan area).</p>
                    
                    <div class="section-heading">Position in Hierarchy:</div>
                    <p>The CJM Court is the apex body of the criminal judiciary at the district level, presiding over all other magistrate courts in the district, including Additional Chief Judicial Magistrates and Judicial Magistrates.</p>
                    
                    <div class="section-heading">Jurisdiction:</div>
                    <p>Original Jurisdiction: The CJM has original jurisdiction in criminal matters arising within the district. It can try offenses punishable with imprisonment for a term not exceeding seven years (Section 29 of CrPC).<br>
                    Territorial Jurisdiction: Defined by the High Court, subject to its control.</p>
                    
                    <div class="section-heading">Powers and Functions:</div>
                    <p>Trial Powers: The CJM can impose any punishment prescribed by law except for death or life imprisonment. The maximum sentence that can be awarded is up to seven years of imprisonment and fines up to ₹10,000.<br>
                    Administrative Role: Acts as the administrative head of all magistrate courts in the district, overseeing their functions and conducting inspections.<br>
                    Preliminary Inquiries: Has the authority to conduct preliminary inquiries into criminal cases, issue search warrants, and grant bail to accused persons.<br>
                    Appeal Jurisdiction: The CJM can hear appeals against judgments from Subordinate Magistrate Courts.</p>
                    
                    <div class="section-heading">Additional Responsibilities:</div>
                    <p>Inspects the courts and offices of other magistrates in the district and makes monthly inspections of jails/lock-ups.<br>
                    Can direct warrants for arrest and handle claims related to property attachment under relevant sections of the CrPC.</p>
                    
                    <div class="section-heading">Summary</div>
                    <p>The Chief Judicial Magistrate plays a crucial role in the criminal justice system at the district level, handling serious offenses, overseeing subordinate courts, and ensuring effective administration of justice. The CJM's powers are significant but do not extend to capital punishment or life sentences.</p>
                `
            },
            metro: {
                title: "Metropolitan Magistrates",
                content: `
                    <p><span class="legal-ref">Established under:</span> Section 16 of the Code of Criminal Procedure (CrPC): This section mandates the establishment of Courts of Metropolitan Magistrates in every metropolitan area, defined as areas with a population exceeding one million.</p>
                    
                    <div class="section-heading">Jurisdiction:</div>
                    <p>Geographical Jurisdiction: The jurisdiction of a Metropolitan Magistrate extends throughout the metropolitan area, allowing them to try offenses committed within that territory.<br>
                    Types of Cases: They can handle a wide range of criminal cases, typically those punishable with imprisonment for a term not exceeding three years.</p>
                    
                    <div class="section-heading">Composition:</div>
                    <p>The presiding officers of these courts are appointed by the High Court. Each metropolitan area will have as many Metropolitan Magistrates as deemed necessary by the State Government in consultation with the High Court.</p>
                    
                    <div class="section-heading">Powers and Functions:</div>
                    <p>Trial Powers: A Metropolitan Magistrate has the powers of a first-class magistrate, which includes trying offenses punishable with imprisonment for up to three years and imposing fines not exceeding ₹10,000 (as per Section 29 of the CrPC).<br>
                    Administrative Role: They operate under the supervision of the Chief Metropolitan Magistrate and are subordinate to them. The Chief Metropolitan Magistrate has regulatory powers over their functions.<br>
                    Special Metropolitan Magistrates: Under Section 18 of the CrPC, Special Metropolitan Magistrates may be appointed with similar powers for specific cases or functions.</p>
                    
                    <div class="section-heading">Sentencing Powers:</div>
                    <p>A Metropolitan Magistrate can impose sentences consistent with those applicable to first-class magistrates, specifically for offenses punishable by up to three years in prison or fines up to ₹10,000.</p>
                    
                    <div class="section-heading">Summary</div>
                    <p>Metropolitan Magistrates serve an essential role in the criminal justice system within metropolitan areas, handling a variety of offenses while operating under the jurisdiction defined by the CrPC. They possess significant trial powers and are integral to maintaining law and order in urban settings. However, they do not have jurisdiction over cases involving more severe penalties, which are reserved for higher courts.</p>
                `
            },
            jmfc: {
                title: "Judicial Magistrate of the First Class (JMFC)",
                content: `
                    <p><span class="legal-ref">Established under:</span> Section 11 of the Code of Criminal Procedure (CrPC): Courts of Judicial Magistrates of the First Class may be established by the State Government in consultation with the High Court.</p>
                    
                    <div class="section-heading">Jurisdiction:</div>
                    <p>Original Jurisdiction: The JMFC has jurisdiction to try offenses punishable with imprisonment for a term not exceeding three years (Section 29 of CrPC).<br>
                    Territorial Jurisdiction: Defined by the district in which they are appointed, excluding metropolitan areas.</p>
                    
                    <div class="section-heading">Powers and Functions:</div>
                    <p>Trial Powers: Can impose sentences up to three years of imprisonment or fines not exceeding ₹10,000.<br>
                    Bail Powers: The JMFC has the authority to grant bail in cases where the offense is punishable by less than seven years' imprisonment.<br>
                    Administrative Role: Operates under the general control of the Sessions Judge and is subordinate to the Chief Judicial Magistrate.</p>
                    
                    <div class="section-heading">Additional Responsibilities:</div>
                    <p>Can issue search warrants and conduct preliminary inquiries into offenses.<br>
                    May also handle cases that require special attention or have been referred from lower courts.</p>
                `
            },
            jmsc: {
                title: "Judicial Magistrate of the Second Class (JMSC)",
                content: `
                    <p><span class="legal-ref">Established under:</span> Section 11 of the CrPC: Courts of Judicial Magistrates of the Second Class may also be established by the State Government in consultation with the High Court.</p>
                    
                    <div class="section-heading">Jurisdiction:</div>
                    <p>Original Jurisdiction: The JMSC can try offenses punishable with imprisonment for a term not exceeding one year (Section 29(3) of CrPC).<br>
                    Territorial Jurisdiction: Similar to JMFC, defined by their district appointment.</p>
                    
                    <div class="section-heading">Powers and Functions:</div>
                    <p>Trial Powers: Can impose sentences up to one year of imprisonment or fines not exceeding ₹5,000 (or higher as specified by state laws).<br>
                    Limitations on Powers: Cannot entertain police remand requests; such cases must be referred to a Judicial Magistrate of the First Class if necessary.</p>
                    
                    <div class="section-heading">Additional Responsibilities:</div>
                    <p>Handles minor offenses and conducts preliminary inquiries.<br>
                    Must have production warrants countersigned by the Chief Judicial Magistrate as per Section 267 of CrPC.</p>
                    
                    <div class="section-heading">Summary</div>
                    <p>Judicial Magistrates of the First Class and Second Class serve vital roles in India's criminal justice system. JMFC handles more serious offenses with greater sentencing powers, while JMSC deals with less severe cases. Both classes operate under a structured hierarchy and contribute to maintaining law and order within their jurisdictions.</p>
                `
            }
        };

        function showDetails(courtType) {
            const contentDiv = document.getElementById('content');
            contentDiv.innerHTML = `
                <h2>${courtData[courtType].title}</h2>
                ${courtData[courtType].content}
            `;
            document.getElementById('detailsPane').style.display = 'block';
            document.getElementById('overlay').style.display = 'block';
        }

        function closeDetails() {
            document.getElementById('detailsPane').style.display = 'none';
            document.getElementById('overlay').style.display = 'none';
        }
    </script>



</body></html>
