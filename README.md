<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard with Top Navigation</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Transcity&display=swap">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Gravity+Wanders&display=swap">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            display: flex;
            flex-direction: column;
            height: 100vh;
        }
        .main-content {
            text-align: center;
            padding: 10px 20px;
            flex-grow: 1;
            overflow-y: auto;
        }
        .home-content, .profile-content, .services-content {
            font-family: 'Transcity', sans-serif;
            color: black;
            margin-top: 0;
            display: none;
        }
        .top-nav {
            display: flex;
            justify-content: center;
            background-color: #1E90FF;
            padding: 5px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .top-nav a {
            color: white;
            text-decoration: none;
            padding: 5px 10px; /* Smaller padding for smaller buttons */
            border-radius: 5px;
            transition: background-color 0.3s;
            margin: 0 2px; /* Add margin between buttons */
        }
        .top-nav a:hover {
            background-color: #1C86EE;
        }
        .intro {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #000;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2em;
            z-index: 1000;
            animation: fadeout 3s forwards;
        }
        @keyframes fadeout {
            0% { opacity: 1; }
            100% { opacity: 0; }
        }
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(30deg); }
        }
        .profile-picture {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            object-fit: cover;
            border: 2px solid #1E90FF;
            margin-bottom: 15px;
        }
        .profile-form {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .profile-form input, .profile-form button {
            padding: 10px;
            width: 80%;
            max-width: 400px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }
        .profile-form button {
            background-color: #1E90FF;
            color: white;
            border: none;
            cursor: pointer;
        }
        .profile-form button:hover {
            background-color: #1C86EE;
        }
        .profile-form input[readonly] {
            background-color: #e9e9e9;
        }
        .service {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }
        .service img {
            width: 100px;
            height: 100px;
            object-fit: cover;
            margin-right: 20px;
            border-radius: 10px;
        }
        .service-description {
            text-align: left;
        }
        .service-description strong {
            font-size: 1.2em;
        }
    </style>
</head>
<body>

<div class="intro">
    <div class="wave" style="animation: wave 3s infinite;">Tales Online Server</div>
</div>

<nav class="top-nav">
    <a href="#" onclick="showSection('home')">Home</a>
    <a href="#" onclick="showSection('services')">Services</a>
    <a href="#" onclick="showSection('notification')">Notification</a>
    <a href="#" onclick="showSection('profile')">Profile</a>
    <a href="#" onclick="showSection('about')">About Developer</a>
</nav>

<div class="main-content">
    <div id="home" class="home-content">
        <p>
            Tales Online is dedicated to providing excellent services to our clients. Our offices offer a variety of resources and support to help individuals and businesses thrive. We are committed to making a positive impact in the communities we serve.
        </p>
        <p>
            Our services are designed to be accessible and helpful to people from all walks of life. Whether you need assistance with technology, business development, or personal growth, Tales Online Offices are here to support you.
        </p>
        <p>
            <strong>Head Office:</strong><br>
            123 Main Street, Nairobi, Kenya<br>
            Phone: +254 700 123 456<br>
            Email: info@talesonline.com
        </p>
        <p>
            <strong>Branch Offices:</strong><br>
            Mombasa: 456 Coastline Road<br>
            Kisumu: 789 Lakeview Avenue<br>
            Eldoret: 101 Highland Drive
        </p>
    </div>

    <div id="services" class="services-content">
        <div class="service">
            <img src="https://assets.onecompiler.app/42jd8ggps/437kssrka/business%20reg.jfif" alt="Business Registration">
            <div class="service-description">
                <strong>Business Registration:</strong>
                Get your business registered quickly and efficiently. We handle the entire process, including name search, reservation, and document submission. Whether you’re starting a sole proprietorship, partnership, or a company, we ensure compliance with local regulations to get you up and running legally.
            </div>
        </div>
        <div class="service">
            <img src="https://assets.onecompiler.app/42jd8ggps/437kssrka/tax%20time.jfif" alt="VAT/Rental Returns">
            <div class="service-description">
                <strong>VAT/Rental Returns:</strong>
                We assist with the preparation and submission of VAT and rental income returns. Our experts help you navigate tax regulations, ensuring accurate reporting and compliance. Stay ahead of deadlines and avoid penalties with our reliable service.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Motor Vehicle Transfer:</strong>
                Simplify the process of transferring vehicle ownership. We handle all necessary paperwork, including filling out forms and liaising with the National Transport and Safety Authority (NTSA) to ensure a smooth transfer. Our service is designed to save you time and hassle.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Good Conduct Certificate:</strong>
                Obtain a certificate of good conduct for employment or travel purposes. We assist with the application process, including fingerprinting and submitting the required documents to the Directorate of Criminal Investigations (DCI). Ensure you meet all the requirements without delays.
            </div>
        </div>
        <div class="service">
            <img src="https://assets.onecompiler.app/42jd8ggps/437kssrka/helb%20img.jfif" alt="HELB Certificate">
            <div class="service-description">
                <strong>HELB Certificate:</strong>
                Apply for your Higher Education Loans Board (HELB) certificate with ease. Our service includes guidance on filling out the application form, submitting necessary documents, and tracking the progress of your application. We aim to make the process as straightforward as possible.
            </div>
        </div>
        <div class="service">
            <img src="https://assets.onecompiler.app/42jd8ggps/437kssrka/visa%20application.jfif" alt="Visa Application">
            <div class="service-description">
                <strong>Visa Application:</strong>
                Planning to travel abroad? We assist with visa applications for various countries, ensuring you meet all the requirements. Our service includes document preparation, application form completion, and appointment scheduling. Travel with confidence knowing your visa application is in good hands.
            </div>
        </div>
        <div class="service">
            <img src="https://assets.onecompiler.app/42jd8ggps/437kssrka/tax.jfif" alt="KRA PIN">
            <div class="service-description">
                <strong>KRA PIN:</strong>
                Get your Kenya Revenue Authority (KRA) PIN for tax purposes. We help with the application process, including filling out the online form and submitting necessary documents. Whether you’re an individual or a business, we ensure you have your KRA PIN for tax compliance.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>AGPO Certification:</strong>
                Access government procurement opportunities by obtaining the Access to Government Procurement Opportunities (AGPO) certificate. We guide you through the application process, ensuring you meet the eligibility criteria and submit all required documents. Increase your chances of winning government tenders.
            </div>
        </div>
        <div class="service">
            <img src="https://assets.onecompiler.app/42jd8ggps/437kssrka/images%20(2).jfif" alt="NHIF Registration">
            <div class="service-description">
                <strong>NHIF Registration:</strong>
                Register for the National Hospital Insurance Fund (NHIF) to access affordable healthcare. Our service includes assistance with filling out the application form, submitting required documents, and ensuring your registration is complete. Stay covered and enjoy the benefits of NHIF membership.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Temporary Permit:</strong>
                Obtain a temporary permit for various purposes, such as business or travel. We assist with the application process, including filling out the required forms and submitting necessary documents. Our goal is to make the process as quick and hassle-free as possible.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>East Africa Passport Application:</strong>
                Apply for an East Africa passport to travel within the region. We guide you through the application process, ensuring you meet all the requirements and submit the necessary documents. Travel freely within East Africa with a valid passport.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Driving Licence Renewal:</strong>
                Renew your driving licence with ease. Our service includes assistance with filling out the renewal application form, submitting required documents, and liaising with the National Transport and Safety Authority (NTSA) to ensure timely renewal. Keep your licence up-to-date without any stress.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Vehicle Search:</strong>
                Conduct a vehicle search to verify ownership and check for any outstanding issues. We assist with the search process, including submitting the necessary forms and liaising with the National Transport and Safety Authority (NTSA). Get accurate and up-to-date information about any vehicle.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Birth Certificate Application:</strong>
                Apply for a birth certificate for yourself or your child. We guide you through the application process, ensuring you submit all required documents and meet the eligibility criteria. Get your birth certificate without any delays or complications.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>TSC Number Application:</strong>
                Obtain a Teachers Service Commission (TSC) number for employment as a teacher in Kenya. Our service includes assistance with filling out the application form, submitting necessary documents, and tracking the progress of your application. Start your teaching career with confidence.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>HELB Loan Application:</strong>
                Apply for a Higher Education Loans Board (HELB) loan to finance your studies. We guide you through the application process, ensuring you meet all the requirements and submit the necessary documents. Access financial support for your education with ease.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Tax Compliance Certificate:</strong>
                Obtain a tax compliance certificate for various purposes, such as business registration or tender applications. Our service includes assistance with the application process, ensuring you meet the eligibility criteria and submit all required documents. Stay compliant with tax regulations.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Vehicle Booking Inspection:</strong>
                Book a vehicle inspection to ensure your vehicle meets safety and regulatory standards. We assist with the booking process, including filling out the necessary forms and scheduling an appointment with the National Transport and Safety Authority (NTSA). Keep your vehicle roadworthy and compliant.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>USA Green Card Application:</strong>
                Apply for a USA Green Card to live and work in the United States. Our service includes assistance with filling out the application form, submitting necessary documents, and preparing for the interview process. Increase your chances of success with our expert guidance.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Driving Licence Application:</strong>
                Apply for a new driving licence with our assistance. We guide you through the application process, including filling out the required forms and submitting necessary documents. Get your driving licence and hit the road with confidence.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>PSV Licence Application:</strong>
                Obtain a Public Service Vehicle (PSV) licence for operating commercial vehicles. Our service includes assistance with filling out the application form, submitting required documents, and liaising with the National Transport and Safety Authority (NTSA). Ensure you meet all the requirements for a PSV licence.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>CR12 Application:</strong>
                Apply for a CR12 document to verify company ownership and structure. We assist with the application process, including filling out the necessary forms and submitting required documents. Get accurate and official information about any company.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Web Design Services:</strong>
                Get a professional website designed for your business or personal use. Our web design service includes creating visually appealing and functional websites, tailored to your specific needs. Enhance your online presence and attract more customers with a well-designed website.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Graphic Design Services:</strong>
                Access creative graphic design services for various purposes, such as branding, marketing, and advertising. We create eye-catching designs that effectively communicate your message and enhance your brand identity. Stand out with professional graphic design.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Software Solutions:</strong>
                Get custom software solutions tailored to your business needs. Our services include software development, implementation, and support. Improve efficiency, streamline processes, and achieve your business goals with our innovative software solutions.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Computer/Laptop Repair:</strong>
                Access reliable computer and laptop repair services. We diagnose and fix hardware and software issues, ensuring your devices are up and running smoothly. Get professional repair services to keep your technology in top condition.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Binding Services:</strong>
                Get your documents professionally bound for a polished and organized presentation. Our binding services include various binding options, such as comb binding, wire binding, and thermal binding. Ensure your documents are neat and presentable.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Lamination Services:</strong>
                Protect and preserve your documents with our lamination services. We laminate various types of documents, such as certificates, identification cards, and posters. Keep your important documents safe and durable.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Printing Services:</strong>
                Access affordable and high-quality printing services for various needs, such as documents, flyers, and posters. Our printing services are available at just 5/- per page. Get your materials printed efficiently and cost-effectively.
            </div>
        </div>
        <div class="service">
            <div class="service-description">
                <strong>Scanning Services:</strong>
                Digitize your documents with our scanning services. We scan various types of documents, ensuring high-quality digital copies for easy storage and access. Keep your documents organized and easily accessible with our scanning services.
            </div>
        </div>
    </div>

    <div id="profile" class="profile-content">
        <h1>Profile</h1>
        <form class="profile-form" onsubmit="saveProfile(event)">
            <input type="file" id="profile-picture-input" accept="image/*" onchange="updateProfilePicture(event)">
            <img src="default-profile.png" id="profile-picture" class="profile-picture" alt="Profile Picture">
            <input type="text" id="first-name" placeholder="First Name" required>
            <input type="text" id="last-name" placeholder="Last Name" required>
            <input type="date" id="dob" required>
            <input type="text" id="id-number"
