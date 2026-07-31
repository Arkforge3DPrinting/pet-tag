# pet-tag
Pet-tag tracking system for NFC tag collar badges.
# Create Pet Tag
https://arkforge3dprinting.github.io/pet-tag/createtag.html
# Find Pets Example
https://arkforge3dprinting.github.io/pet-tag/?id=z10y6gx8yp
# Customer Activation Link Example
https://arkforge3dprinting.github.io/pet-tag/activate.html?id=z10y6gx8yp
# Image Storage
https://console.cloudinary.com/app/c-9871aeeea5113607acffe58db4fc41/home/dashboard
# Admin Board
https://arkforge3dprinting.github.io/pet-tag/login.html

# ArkLink Pet ID Tag Manufacturing SOP

## Unique QR Code Generation & 3D Printing Process

### Purpose

This procedure outlines the process for creating unique ArkLink Pet ID tags, generating the corresponding QR codes, and preparing the 3D model for printing.

---

# 1. Create Unique ArkLink Tag ID

Each physical ArkLink tag must have its own unique identifier.

Example:

```
AL-0001
AL-0002
AL-0003
```

The tag ID should be recorded and linked to the corresponding pet profile in the ArkLink database.

---

# 2. Create Unique Activation Link

For each new tag, generate a unique activation URL.

Example:

```
https://arkforge3dprinting.github.io/pet-tag/activate.html?id=AL-0001
```

Each tag must have its own unique ID within the URL.

Example:

Tag AL-0001:

```
https://arkforge3dprinting.github.io/pet-tag/activate.html?id=AL-0001
```

Tag AL-0002:

```
https://arkforge3dprinting.github.io/pet-tag/activate.html?id=AL-0002
```

---

# 3. Generate QR Code

1. Open QR Code Generator:

https://www.qrcode-monkey.com/

2. Enter the unique ArkLink activation URL.

3. Generate the QR code.

4. Download the QR code as a PNG file.

Recommended naming format:

```
AL-0001_QR.png
AL-0002_QR.png
```

---

# 4. Convert QR Code PNG to SVG

SVG format is preferred for Bambu Studio because it maintains quality when resized.

1. Open:

https://convertio.co/

2. Upload the QR PNG file.

3. Convert:

```
PNG → SVG
```

4. Download the SVG file.

Recommended naming format:

```
AL-0001_QR.svg
AL-0002_QR.svg
```

---

# 5. Update ArkLink 3D Model in Bambu Studio

1. Open the ArkLink master model in Bambu Studio.

2. Select the existing QR code object.

3. Choose:

```
Replace / Edit Object
```

4. Import the new SVG QR code.

5. Position and scale the QR code correctly.

6. Confirm the QR code is readable.

---

# 6. Slice and Print

1. Select the correct printer profile.

2. Slice the model.

3. Preview the print.

4. Confirm:

* QR code is present
* QR code is correctly positioned
* No layer issues

5. Send print job.

---

# 7. Record Completed Tag

After printing, update inventory records:

Example:

| Tag ID  | QR Link                  | Status  |
| ------- | ------------------------ | ------- |
| AL-0001 | activate.html?id=AL-0001 | Printed |
| AL-0002 | activate.html?id=AL-0002 | Printed |

The physical tag is now ready for activation and customer use.

---

# Future Automation Opportunity

When sales volume increases, this process can be automated:

Order received
↓
Generate unique AL ID
↓
Generate QR code automatically
↓
Convert to SVG
↓
Insert into Bambu Studio template
↓
Print

Until then, this manual workflow provides full control and ensures every ArkLink tag remains unique.
