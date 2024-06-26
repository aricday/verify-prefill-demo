### Introducing Identity Pre-Fill with Twilio Lookup API: Streamline User Experiences

#### By Aric Day (Twilio SE)

The Twilio Lookup API offers a set of packages that can help businesses provide a secure and seamless experience for initial user registration, login, consent capture and other business processes.  The Lookup API allows businesses to access user identity signals utilizing the provided phone numbers from the users.  Twilio Lookup packages are currently available for a variety of signals including: Carrier and Line Type Intelligence, SIM Swap, SMS Pumping Risk and Identity Match.

In today's digital age, user experience is paramount. Every additional step or friction point can deter potential customers, reduce conversion rates, and degrade the overall experience. To combat this, Twilio introduces an innovative feature within its Lookup API: **Identity Pre-Fill** in Private Beta. This powerful tool can revolutionize how businesses handle customer interactions, from onboarding to checkout, by pre-populating user data with verified information. Below, we discuss how this feature works, its potential benefits, and ways you can leverage it through a sample demo app.


### What is Identity Pre-Fill?



**Identity Pre-Fill** is a new pilot preview capability in the Twilio Lookup API that provides the first name, last name, and address of end-users after verifying their phone number possession using Twilio Verify. This data helps pre-populate forms, making the user experience smoother and faster by reducing manual input efforts.



#### Value Propositions



1. **Frictionless Customer Onboarding**:

   - **Scenario**: During onboarding, reducing user effort is crucial. During your onboarding process, start by requesting the consumer phone number. Using Twilio Verify, verify the number, and once verified, supply the Verification SID to the Lookup Pre-Fill API. In return, get the user’s first name, last name, and address.

   - **Benefit**: This reduces friction and speeds up the onboarding process, enhancing the user experience. Auto-populating user data (name and address) reduces friction and increases conversion rates.



2. **Streamline Customer Checkout**:

   - **Scenario**: During checkout, customers provide a phone number that's verified via Twilio Verify. Once the verification is approved, use Prefill to populate the name and address fields instantly.  Around 70% of shoppers abandon carts, with even higher rates on mobile.

   - **Benefit**: This quickens the checkout process, reducing cart abandonment rates.  With a verified phone number, you can auto-populate the name and shipping/billing address, which can lead to higher checkout conversion rates.



3. **Reduce Time and Effort**:

   - **Scenario**: Filling out forms often feels burdensome to users. With Identity Pre-Fill, forms auto-populate with the verified user's details.

   - **Benefit**: Less perceived effort and time to fill out forms, leading to a smooth user interaction.



4. **Avoid Misspellings**:

   - **Scenario**: Manually entering information can lead to errors.

   - **Benefit**: Automatically filled forms ensure accuracy in user details, reducing errors like misspellings of names or addresses.



5. **Increase Conversion Rate**:

   - **Scenario**: Reducing the number of steps in any process lowers interaction costs.

   - **Benefit**: A smoother user experience leads to higher conversion rates because users can navigate through forms easily.



### Demo App: Verify Prefill Demo



To showcase these benefits, we've created a demo app called [Verify Prefill Demo](https://github.com/aricday/verify-prefill-demo). This app demonstrates how you can leverage the Identity Pre-Fill feature in real-world scenarios.



#### How It Works:

1. **Enter Phone Number**: Users input their phone number.

2. **Send OTP**: An OTP is sent to the phone number via Twilio Verify.

3. **Verify OTP**: Users enter the OTP received.

4. **Fetch and Prefill Data**: Upon successful verification, the app fetches the user’s first name, last name, and address using the Lookup API and automatically fills in the fields.


Try the [Verify Prefill Demo](https://github.com/aricday/verify-prefill-demo) on GitHub to see how easy it is to integrate this powerful feature into your applications!


### Technical Details



A few technical aspects to keep in mind:

- Queries to the Identity Pre-Fill API are only accepted within 10 minutes of successful verification through Twilio Verify.

- This product is only available in the United States during the pilot phase.

- Use of this product requires the use of the Twilio Verify product. Customers using custom code implementations for verification are not eligible for the pilot.



### Conclusion



Identity Pre-Fill is a game-changer for businesses looking to enhance user experiences and streamline processes. By reducing the effort required to fill out forms and ensuring data accuracy while speeding up interactions, you can significantly improve customer satisfaction and conversion rates.



Visit our [Verify Prefill Demo](https://www.twilio.com/code-exchange/verify-lookup-identity-prefill) on Twilio's Code Exchange and get started with integrating Identity Pre-Fill into your system. Enhance your user experience and keep your customers delighted with Twilio’s Lookup API.



#### Learn More

For detailed documentation and more information on Identity Pre-Fill, visit the [Twilio Lookup API documentation](https://www.twilio.com/docs/lookup/api).
