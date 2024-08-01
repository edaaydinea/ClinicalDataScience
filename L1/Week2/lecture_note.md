# Introduction to Clinical Data

1. **Difference Between EHRs and EMRs**
    - EHR (Electronic Health Record): Comprehensive, includes medical records from multiple providers, radiology images, laboratory data, insurance information, patient demographics, genetic sequencing, and fitness tracker data.
    - EMR (Electronic Medical Record): Limited, electronic version of a paper chart, usually limited to a single set of providers, not easily shared.
    - EHR is much broader and more useful tool that an EMR.
    
    <aside>
    ❓ What types of data are available in an EHR, but not an EMR?
    - The notes of multiple types of providers
    - Radiology data
    - Laboratory Test Data
    - Insurance and Billing Information
    
    </aside>
    
2. **Purpose of EHRs**
    - Patient care: Diagnoses, medications, allergies, laboratory tests, radiology images, hospitalization details.
    - Billing and payment: Documenting medical care provided, services rendered, and justification.
        - What was performed?
        - By whom?
        - For what purpose?
    - Legal record: Recording provider knowledge, data entry, review history, and health privacy compliance.
        - Who recorded data?
        - Who saw what when?
        - Audit logs
3. **Four W's Framework for Clinical Data**
    - **Who recorded the information?**
        - Front desk staff, nurses, providers, residents, lab technicians, pharmacists.
    - **When was the information recorded?**
        - Providers may finalize notes days later, laboratory data may have multiple dates (order date, lab draw date, result availability, provider review date).
    - **Why was the information recorded?**
        - Clinical care (e.g., lab test order), billing code for reimbursement, clinical notes for billing and legal records.
    - **What was recorded?**
        - Structured data: Single numbers or limited options.
        - Semi-structured data: Spreadsheet-like, data in specific locations (could be numbers, words, paragraphs).
        - Unstructured data: Free form text without obvious structure.

---

1. **EHR ve EMR Arasındaki Fark**
    - EHR (Elektronik Sağlık Kaydı): Kapsamlı, birden fazla sağlayıcıdan tıbbi kayıtlar, radyoloji görüntüleri, laboratuvar verileri, sigorta bilgileri, hasta demografisi, genetik dizilim ve fitness takip cihazı verilerini içerir.
    - EMR (Elektronik Tıbbi Kayıt): Sınırlı, kağıt şemsiye elektronik versiyonu, genellikle tek bir sağlayıcı seti ile sınırlıdır, kolayca paylaşılamaz.
2. **EHR'lerin Amacı**
    - Hasta bakımı: Teşhisler, ilaçlar, alerjiler, laboratuvar testleri, radyoloji görüntüleri, hastane detayları.
    - Faturalandırma ve ödeme: Sağlanan tıbbi bakımın, hizmetlerin ve gerekçelerin belgelenmesi.
    - Hukuki kayıt: Sağlayıcı bilgisi, veri girişi, gözden geçirme geçmişi ve sağlık gizliliği uyumluluğu.
3. **Klinik Veri İçin Dört W Çerçevesi**
    - **Bilgiyi kim kaydetti?**
        - Resepsiyon görevlisi, hemşireler, sağlayıcılar, asistanlar, laboratuvar teknisyenleri, eczacılar.
    - **Bilgi ne zaman kaydedildi?**
        - Sağlayıcılar notlarını günler sonra tamamlayabilir, laboratuvar verileri birden fazla tarih içerebilir (sipariş tarihi, laboratuvar çekim tarihi, sonuç kullanılabilirliği, sağlayıcı inceleme tarihi).
    - **Bilgi neden kaydedildi?**
        - Klinik bakım (örneğin, laboratuvar test siparişi), faturalandırma kodu için, klinik notlar faturalandırma ve hukuki kayıtlar için.
    - **Ne kaydedildi?**
        - Yapılandırılmış veri: Tek numaralar veya sınırlı seçenekler.
        - Yarı yapılandırılmış veri: Elektronik tablo benzeri, belirli yerlerde veri (numaralar, kelimeler, paragraflar olabilir).
        - Yapılandırılmamış veri: Belirgin yapısı olmayan serbest metin.

# Encounters

1. **EHRs and Encounters**
    - Modern EHRs focus on events or encounters.
    - A new encounter is created each time there is contact with a healthcare provider (in-person, phone, online).
2. **Classifying Encounters by Contact Type**
    - **In-person encounters:**
        - **Outpatient encounters:** Visits to a provider’s office without hospital admission.
            - Examples: Primary care visits, specialist visits, physical therapy, small surgical procedures.
            - Timing classifications: New patient encounters, follow-up appointments, consults.
                - First visit - “New Patient”
                - Second visit - “Follow up appointment”
            - Documentation: Single note, vital signs, laboratory tests, medications.
            - Outpatient surgeries: Notes from the surgeon, anesthesiology team, pre/post-operative care, medication records.
        - **Inpatient encounters:** Hospital admissions for intensive treatment.
            - Duration: Start (admission time) to end (discharge time).
            - Involves many healthcare team members: Physicians, nurses, pharmacists, physical therapists, social workers.
            - Documentation: Admission and discharge notes, daily summaries, vital signs data from machines.
                - Many unstructured notes
                - Structured monitoring data & complex sensor data
        - **Emergency room encounters:** Ranges from simple outpatient care to severe trauma requiring surgery and admission.
    - **Phone and electronic encounters:**
        - **Phone visits and eConsults:** Classified similarly to outpatient encounters.
        - **Messages (phone or secure email):** Different encounter type, can occur between patient and provider or care team members.
3. **Who, Why, and When of Encounters**
    - Encounter information is often automatically generated in EHRs.
    - **Who:** Typically assigned by scheduling staff.
    - **Why and When:** Captured as part of the EHR data entry process.

---

1. **EHR'ler ve Karşılaşmalar**
    - Modern EHR'ler olaylara veya karşılaşmalara odaklanır.
    - Her sağlık hizmeti sağlayıcısıyla temas edildiğinde (yüz yüze, telefon, çevrimiçi) yeni bir karşılaşma oluşturulur.
2. **Temas Türüne Göre Karşılaşmaların Sınıflandırılması**
    - **Yüz yüze karşılaşmalar:**
        - **Ayakta tedavi karşılaşmaları:** Hastane yatışı olmadan sağlayıcı ofisine yapılan ziyaretler.
            - Örnekler: Birincil bakım ziyaretleri, uzman ziyaretleri, fizik tedavi, küçük cerrahi işlemler.
            - Zamanlama sınıflandırmaları: Yeni hasta karşılaşmaları, takip randevuları, danışmalar.
            - Belgeleme: Tek not, yaşamsal belirtiler, laboratuvar testleri, ilaçlar.
            - Ayakta tedavi ameliyatları: Cerrah, anestezi ekibi, ön/son bakım notları, ilaç kayıtları.
        - **Yatarak tedavi karşılaşmaları:** Yoğun tedavi için hastane yatışları.
            - Süre: Başlangıç (yatış zamanı) ve bitiş (taburcu zamanı).
            - Birçok sağlık ekibi üyesini içerir: Hekimler, hemşireler, eczacılar, fizik tedavi uzmanları, sosyal hizmet uzmanları.
            - Belgeleme: Yatış ve taburcu notları, günlük özetler, makinelerden alınan yaşamsal belirtiler verileri.
        - **Acil servis karşılaşmaları:** Basit ayakta tedaviden ciddi travmalara kadar uzanır, ameliyat ve yatış gerektirebilir.
    - **Telefon ve elektronik karşılaşmalar:**
        - **Telefon ziyaretleri ve eConsults:** Ayakta tedavi karşılaşmaları gibi sınıflandırılır.
        - **Mesajlar (telefon veya güvenli e-posta):** Farklı karşılaşma türü, hasta ve sağlayıcı veya bakım ekibi üyeleri arasında olabilir.
3. **Karşılaşmaların Kim, Neden ve Ne Zamanı**
    - Karşılaşma bilgileri genellikle EHR'lerde otomatik olarak oluşturulur.
    - **Kim:** Genellikle planlama personeli tarafından atanır.
    - **Neden ve Ne Zaman:** EHR veri girişi sürecinin bir parçası olarak yakalanır.

# Billing Data

1. **Billing Data in Clinical Data Science**
    - Two types of structured data: procedure codes and diagnosis codes.
    - **Procedure codes:** Document what the provider did.
    - **Diagnosis codes:** Document what the procedure was treating and why it was necessary.
2. **Procedure Codes**
    - **CPT codes:** Current Procedural Terminology.
        - Thousands of medical, surgical, radiologic, and laboratory services.
        - Each service has a single five-digit code.
        - Office visits have multiple codes based on scope, complexity, and length.
        - Codes must be justified by the medical record.
        - Developed and maintained by the American Medical Association (AMA).
        - Full list access requires payment due to copyright.
3. **Diagnosis Codes**
    - **ICD codes:** International Classification of Disease.
        - Used for tracking morbidity and mortality and billing in the U.S.
        - Types: ICD9-CM and ICD10-CM.
        - CM in each case stands for Clinical Modification and are meant to distinguish them from the international versions of ICD9 and ICD10.
        - **ICD9-CM:**
            - Structured 5-digit code
            - Five-digit code with a period separating the first three digits from the last two.
                - The first three digits represent the category of the code
                - The second last digits provide additional specificity on things like the location, complexity or origin of the condition.
            - Over 14,000 diagnoses.
        - **ICD10-CM:**
            - Structured, Alphanumeric, 6 to 7 characters in length.
                - The first three characters represent the category.
                - The remaining three to four characters represent the location, severity, or origin of the disease.
            - Nearly 70,000 codes.
            - Increased specificity in location, severity, origin, and type of visit.
            - W59.22XA → means struck by turtle, initial encounter
4. **Assigning Billing Codes**
    - **Who:**
        - Outpatient setting: Physician selects CPT and ICD codes.
        - Hospitalized patients: Professional medical coders.
    - **When:**
        - Outpatient: Billing codes assigned at the time of service or shortly after.
        - Hospital: Final codes chosen after the hospital stay.
    - **Why:** To obtain maximum appropriate reimbursement for the care provided.

---

1. **Klinik Veri Biliminde Faturalandırma Verileri**
    - İki tür yapılandırılmış veri: prosedür kodları ve tanı kodları.
    - **Prosedür kodları:** Sağlayıcının ne yaptığını belgelemek.
    - **Tanı kodları:** Prosedürün neyi tedavi ettiğini ve neden gerekli olduğunu belgelemek.
2. **Prosedür Kodları**
    - **CPT kodları:** Güncel Prosedür Terminolojisi.
        - Binlerce tıbbi, cerrahi, radyolojik ve laboratuvar hizmeti.
        - Her hizmetin tek bir beş haneli kodu vardır.
        - Ofis ziyaretleri kapsam, karmaşıklık ve uzunluğa göre birden fazla koda sahiptir.
        - Kodlar, tıbbi kayıtla gerekçelendirilmelidir.
        - Amerikan Tabipler Birliği (AMA) tarafından geliştirilmiş ve korunmuştur.
        - Tam listeye erişim, telif hakkı nedeniyle ödeme gerektirir.
3. **Tanı Kodları**
    - **ICD kodları:** Uluslararası Hastalık Sınıflandırması.
        - Morbidite ve mortaliteyi izlemek ve ABD'de faturalandırma için kullanılır.
        - Türler: ICD9-CM ve ICD10-CM.
        - **ICD9-CM:**
            - İlk üç basamak ile son iki basamak arasında bir nokta bulunan beş haneli kod.
            - 14.000'den fazla tanı.
        - **ICD10-CM:**
            - Alfanümerik, altı ila yedi karakter uzunluğunda.
            - Yaklaşık 70.000 kod.
            - Konum, şiddet, köken ve ziyaret türünde artan özgüllük.
4. **Faturalandırma Kodlarının Atanması**
    - **Kim:**
        - Ayakta tedavi ortamı: Hekim CPT ve ICD kodlarını seçer.
        - Hastanede yatan hastalar: Profesyonel tıbbi kodlayıcılar.
    - **Ne Zaman:**
        - Ayakta tedavi: Faturalandırma kodları hizmet sırasında veya kısa süre sonra atanır.
        - Hastane: Nihai kodlar hastane konaklamasından sonra seçilir.
    - **Neden:** Sağlanan bakım için en uygun geri ödemeyi almak.

# Laboratory Data

1. **Introduction to Laboratory Measurements**
    - Used to measure specific features of a patient's body and tissue.
    - Helps providers diagnose disease, plan and manage treatments, and track overall health.
    - Valuable for analytics due to their objectivity.
2. **Categories of Lab Tests**
    - **Anatomic Pathology:** Examines organs and tissues.
        - Describes tissue appearance visually or under a microscope.
        - Tests biochemical and molecular properties of tissues.
    - **Clinical Pathology (Laboratory Medicine):** Tests bodily fluids like blood and urine.
        - **Clinical Chemistry:** Measures different chemicals and proteins.
        - **Microbiology:** Identifies infectious agents.
        - **Hematology:** Examines and counts types of blood cells.
        - **Molecular Diagnostics (DNA tests):** Can fall under anatomic or clinical pathology depending on the sample type.
3. **Data Types from Lab Tests**
    - **Anatomic Pathology & Molecular Diagnostics:** Results are unstructured or semi-structured reports.
    - **Clinical Pathology:** Results are often numbers or limited choices (e.g., present/absent) and are structured.
4. **Generating Laboratory Data: The Four Steps**
    - **Step 1: Ordering the Laboratory Test**
        - **Who:** Ordered by a healthcare provider based on the patient's symptoms or for screening purposes.
        - **What:** Lab orders can be specific tests (e.g., sodium or potassium levels) or panels (e.g., basic and complex metabolic panels).
        - **Why:** To gather more information to assess or treat the patient.
        - **When:** When the provider needs additional information based on patient symptoms or for routine screening.
    - **Step 2: Patient Sample Collection**
        - **Who:** Patient interacts with a lab technician who processes the lab order.
        - **What:** Samples (specimen types) like blood, urine, stool, etc.
        - **How:** Method of collection (e.g., blood from an arm or finger stick, random urine collection or 24-hour urine collection).
    - **Step 3: Analyzing the Sample**
        - **Who:** Laboratory staff and pathologists.
        - **Where:** In-house testing (quick results) or send-out labs (longer results time).
        - **How:** Samples are processed according to protocols, which may involve different additives in collection tubes.
        - **What:** Different techniques to measure chemicals or proteins, protocols for handling and processing samples.
    - **Step 4: Returning the Test Results**
        - **Who:** Results returned to the ordering provider.
        - **What:** Key data elements returned include specimen and collection types, lab test name, test results, and reference ranges.
        - **When:** Multiple dates such as test order date, specimen collection date, and result availability date.
5. **Laboratory Information Management System (LIMS)**
    - Stores data elements from steps two and three.
    - Includes specimen type, method of collection, testing protocol, results, and sample tracking information.
6. **Clinical Pathology Results Format**
    - Often include a reference range, indicating normal expected results.
    - May provide specific dates related to the test order, specimen collection, and result availability.

# Medication Data

1. **Introduction to Medications**
    - Medications are drug therapies used to treat or prevent diseases.
    - They come in various forms: pills, injections, creams, shampoos, eye drops, etc.
    - Medications can be combinations of multiple drugs in a single pill.
    - They vary in concentration, dosage, and administration setting (home, inpatient, or outpatient).
2. **Types of Medication Records**
    - **Prescription Records:** Authorization for a patient to receive a drug.
    - **Dispensing Records:** Pharmacy records of filling a drug prescription.
    - **Administration Records:** Records of administering the medication to the patient.
3. **Prescription Records**
    - **What:** Lists the drug, dosage, frequency, and duration.
    - **Who:** Written by a medical provider (doctor, nurse, pharmacist).
    - **How:** Can be a paper record or electronically filed.
    - **Why:** To authorize and specify the treatment plan for the patient.
    - **When:** Typically written during an in-person encounter; refills may be requested electronically or via phone.
4. **Dispensing Records**
    - **What:** Details the drug and amount dispensed to the patient.
    - **Who:** Handled by pharmacies (hospital or community pharmacies like Walgreens or CVS).
    - **Why:** For insurance reimbursement and regulatory compliance.
    - **When:** When the prescription is filled and the drug is handed to the patient.
5. **Administration Records**
    - **What:** Records the type of drug, amount given, and details of the administration.
    - **Who:** Performed and recorded by nursing staff.
    - **Why:** To ensure the care team knows the medication was administered.
    - **When:** At the time of drug administration in a clinical or hospital setting.
6. **Data Elements in Medication Records**
    - **Drug Names:**
        - **Brand Name:** Name given by the original manufacturer (e.g., Lipitor).
        - **Generic Name:** Active ingredient name (e.g., atorvastatin).
            - Same active ingredient
            - Different inactive ingredients
            - Many manufacturers
    - **Strength and Form:**
        - Strength: Concentration of the drug (e.g., 10, 20, 40, 80 mg).
        - Form: Physical form of the drug (e.g., pill, injection).
    - **Route:** How the drug should be administered (e.g., orally, IV, topically).
        - By mouth
        - Intravenous
        - Injection
        - Topically
    - **Dose Amount:** How much of the drug to take each time (e.g., one tablet).
        - How many
        - How much
    - **Frequency:** How often to take the drug (e.g., daily, twice a day).
    - **Duration:** Length of time to take the drug (e.g., 5-10 days for antibiotics).
7. **Complex Medication Therapies**
    - May involve additional data elements not covered in the basic framework.
    - More detailed patient instructions may be included for complex therapies.
8. **Summary of Key Points**
    - Medication records are essential for tracking and managing patient treatments.
    - Different types of records (prescriptions, dispensing, administration) serve various purposes.
    - Understanding the data elements in medication records is crucial for clinical data analysis.

By understanding these elements, a clinical data scientist can effectively manage and analyze medication data to support patient care and treatment outcomes.

# Clinical Observation Data

1. **Introduction to Clinical Observations**
    - Clinical observations are measurements about a patient recorded during healthcare encounters.
    - They include basic measurements like height and weight, and vital signs like temperature and blood pressure.
    - These observations provide insight into a patient’s general health status.
2. **Scope and Scale of Clinical Observations**
    - **Outpatient Visits:**
        - Typically include height, weight, and vital signs.
        - Specialist visits may include additional tests (e.g., lung function tests in pulmonology).
        - Recorded by medical assistants or nurses at the start of an appointment.
    - **Inpatient Visits:**
        - Include more extensive observations throughout the hospital stay.
        - Continuous monitoring (e.g., heart rate, EKG) is common.
        - Nurses and other care team members collect various observations.
        - Include records of food and liquid intake and output.
3. **Types of Clinical Observations**
    - **Vital Signs:**
        - Temperature
        - Blood pressure
        - Heart rate
        - Respiratory rate
    - **Basic Measurements:**
        - Height
        - Weight
        - BMI (Body Mass Index)
    - **Specialist Measurements:**
        - Lung function tests (e.g., spirometry)
        - Allergy tests
        - Other condition-specific tests
4. **Purpose and Importance of Clinical Observations**
    - To assess general health status before a provider sees the patient.
    - To monitor and detect changes in a patient’s condition.
    - To provide data for tracking patient health over time.
    - To assist in diagnosing and managing diseases.
5. **Collection and Recording of Clinical Observations**
    - **Outpatient Settings:**
        - Measurements taken at the beginning of an appointment.
        - Recorded by medical assistants or nurses.
    - **Inpatient Settings:**
        - Continuous and regular measurements throughout the stay.
        - Collected by nurses, respiratory therapists, and other care team members.
        - Includes both automated data (e.g., continuous monitoring) and manually recorded data.
6. **Data Storage and Value**
    - Clinical observations are often stored as structured data.
    - Structured data format makes them highly valuable for analytics.
    - Can be used to identify trends, predict outcomes, and support clinical decisions.

# Demographics, Social and Family History

### Patient Demographics, Social and Family History in Electronic Medical Records

1. **Introduction to Patient Demographics**
    - **Purpose:** Understanding patient demographics helps to assess health risks and tailor medical care.
    - **Key Elements:**
        - **Age:** Standardized and recorded by date of birth.
        - **Race and Ethnicity:** Collection methods vary by health center or clinic. Can be self-reported by patients or observed by staff.
2. **Collection Methods for Race and Ethnicity**
    - **Self-Identification:** Patients personally identify their race and ethnicity.
    - **Staff Observation:** Check-in staff record based on their observations.
3. **Social History**
    - **Purpose:** Provides context about a patient’s life and lifestyle, impacting their health and care plans.
    - **Life Characteristics:**
        - **Occupation and Place of Work:** Indicates patient’s work environment and potential health risks.
        - **Marital Status:** Offers insight into the patient’s support system and obligations.
    - **Lifestyle Characteristics:**
        - **Tobacco Use:** Impacts overall health and disease risk.
        - **Alcohol Consumption:** Affects health risk and medication interactions.
        - **Non-Prescription Drug Use:** Influences health outcomes and treatment plans.
4. **Recording Methods for Social History**
    - **Life Characteristics:** Often recorded in unstructured clinical notes and updated less frequently.
    - **Lifestyle Characteristics:** Typically assessed at every visit and recorded as structured data, though they may also appear in unstructured notes.
5. **Family History**
    - **Purpose:** Identifies genetic health risks by reviewing the health status of parents, siblings, and grandparents.
    - **Collection Methods:**
        - **Structured Fields:** Increasingly used by health systems for proactive data collection.
        - **Unstructured Notes:** Historically captured by physicians in clinical notes.