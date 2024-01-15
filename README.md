# Qath Documentation

Qath was officially shut down and had its servers decommissioned on Jan 6, 2024. The purpose of this repository is to archive all the notes and progress in case the project will spin up again in the future.

It's unfortunate that this is happening but largely it's due to 2 reasons:
- Timing -> Even though the adoption of post-quantum cryptography is inevitable, launching a company/product needs to be timed properly. I have a feeling that its going to be very hard to sell this sort of product when the security risk seems so far into the future. AKA - trying to convince companies (particularly in the contemporary economic circumstances) to spend money on this product seems non-trivial at best.
- Domain Experience -> Security is a tough space and unlike others in the sense that there can't be any problems with the product. If companies are going to trust us with the encryption of their data, then it had better work correctly all the time. Given that this area is a 'greenfield' of sorts, there's not many resources out there on how to start getting involved in this space. I also don't have any mentors/buddies that have domain experience in this space - add on the duties of compliance certifications that a lot of target industries would require (HIPA, FIPS, etc), and it becomes very unsustainable.

A part of me is saying that I didn't really give this attempt a fair shot, but I'm working on a timeline and have already found another idea I want to start executing upon. Nevertheless, going to archive all the items from Notion here so I can delete the teamspace.

## Intro

v2 - Qath is a fully managed software-as-a-service that enables enterprises of all sizes to achieve seamless post-quantum cryptographic agility.

### Why Now?

One of the most important factors in the success of a startup is timing. [This video](https://www.youtube.com/watch?v=bNpx7gpSqbY) is a great explainer. Here are some highlights:

- AirBnb & the 2008 recession
- Z.com as a predecessor to YouTube and availability of high speed internet
- General Magic’s attempt to be the first smartphone

On a more fundamental level, [Garry Tan](https://www.youtube.com/watch?v=LioyyxLgfXQ) said great startup ideas arise in 3 different forms:

- New technology
- New behaviour
- New regulation

**Of these three, new technology and new regulation form the nexus in which Qath can achieve product market fit.**

### New technology

Specifically, research and development in the quantum computing space has been on the rise - especially recently. A few highlights below just taking number of qubits as a metric.

- In late 2019, Google claimed [quantum supremacy](https://en.wikipedia.org/wiki/Quantum_supremacy) (which has since been challenged and conceded) with its Sycamore quantum chip at 53 qubits.
- In October 2021, Chinese researchers demonstrated “*Jiuzhang 2*” - claimed to solve a problem in 1 millisecond that would have taken a classical computer 30 trillion years. Also “*Zuchongzhi 2*” at 66 qubits.
- In November 2021, IBM debuted the Eagle system, at 127 qubits.
- Just a year later in November 2022, IBM announced the debut of Osprey - the world’s largest quantum computer at 433 qubits.

It is trivial to note that the rate at which quantum computing and research is progressing is striking. This is of critical importance as since the dawn of computing, the world is used to classical computers and all of the systems that power the world wide web depend on those classical principles.

As this paradigm shift occurs, these classical principles will be put to the test - and accordingly, so will the systems built around it. Qath aims to focus on the forefront problem of this shift - encryption.

### New regulation

Post-quantum cryptography (PQC) refers to [cryptographic](https://en.wikipedia.org/wiki/Cryptographic_primitive) algorithms (usually [public-key](https://en.wikipedia.org/wiki/Public-key_cryptosystem) algorithms) that are thought to be secure against a [cryptanalytic attack](https://en.wikipedia.org/wiki/Cryptanalytic_attack) by a [quantum computer](https://en.wikipedia.org/wiki/Quantum_computing) (from Wikipedia).

Given the rate at which quantum development is progressing, guidance and regulation by federal authorities (foreign and domestic) regarding the standard at which data and authentication are protected is almost an inevitability. 

In fact, the writing is on the wall:

- [March 2021](https://www.dhs.gov/news/2021/03/31/secretary-mayorkas-outlines-his-vision-cybersecurity-resilience) - Alejandro Mayorkas, Secretary of Homeland Security identified the transition to post-quantum encryption as a priority
- [May 2022](https://www.whitehouse.gov/briefing-room/statements-releases/2022/05/04/national-security-memorandum-on-promoting-united-states-leadership-in-quantum-computing-while-mitigating-risks-to-vulnerable-cryptographic-systems/) - The White House outlined its goals to maintain the nation's competitive advantage in quantum information science (QIS). Specifically:
    
    > **From [National Security Memorandum 10](https://www.whitehouse.gov/briefing-room/statements-releases/2022/05/04/national-security-memorandum-on-promoting-united-states-leadership-in-quantum-computing-while-mitigating-risks-to-vulnerable-cryptographic-systems/)**:
    > 
    > 
    > Sec. 3.  Mitigating the Risks to Encryption.  (a)  Any digital system that uses existing public standards for public‑key cryptography, or that is planning to transition to such cryptography, could be vulnerable to an attack by a CRQC.  To mitigate this risk, the United States must prioritize the timely and equitable transition of cryptographic systems to quantum-resistant cryptography, with the goal of mitigating as much of the quantum risk as is feasible by 2035.  Currently, the Director of the National Institute of Standards and Technology (NIST) and the Director of the National Security Agency (NSA), in their capacity as the National Manager for National Security Systems (National Manager), are each developing technical standards for quantum‑resistant cryptography for their respective jurisdictions.  The first sets of these standards are expected to be released publicly by 2024.
    > 
    > (b)  Central to this migration effort will be an emphasis on cryptographic agility, both to reduce the time required to transition and to allow for seamless updates for future cryptographic standards.  This effort is an imperative across all sectors of the United States economy, from government to critical infrastructure, commercial services to cloud providers, and everywhere else that vulnerable public-key cryptography is used.
    > 
- [Originally retrieved July 2022](https://www.nsa.gov/Cybersecurity/Quantum-Key-Distribution-QKD-and-Quantum-Cryptography-QC/) - the NSA releases a recommendation for PQC over other quantum key distributions (QKD). Similar recommendations issued by the relevant agencies from the EU, UK, and France.
- [July 2022](https://www.cisa.gov/news-events/news/cisa-announces-post-quantum-cryptography-initiative) - CISA (Cybersecurity and Infrastructure Security Agency) announced the [PQC Initiative](https://www.cisa.gov/quantum), that aims to “*unify and drive efforts with interagency and industry partners to address threats posed by quantum computing and to support critical infrastructure and government network owners and operators during the transition to post-quantum cryptography*”.
- July 2022 and ongoing - the NIST released the first 4 algorithms it qualifies as quantum safe. An effective green light for implementation.

Such measures are pointing to PQC as a north star for the new standard of encryption across the entire computing industry. Qath should be well-positioned to carve out a sizeable portion of the market as this paradigm shift is taking place.

### Why Us?

- Engineers professionally and friends at heart.
- Very low market penetration right now. In market research, a few companies seemed to be doing some form of this already.
    - In the US (QuSecure)
        - Has secured partnerships with AWS, US AirForce, RedHat, among some other financial and technology firms
        - Provide two products as part of their QuProtect suite - QuEverywhere (secure Web Application communication) and QuNetwork (secure server to server communication)
        - Funding is ~13M, but is also a subsidiary of Quantum Thought, that describes itself as “Quantum Thought is the world's leading incubator for creating and commercializing quantum computing intellectual property, products, and companies. Based in Silicon Valley, Quantum Thought has assembled an unparalleled team of leaders, quantum programmers, and analysts who have already created significant quantum technologies in medical imaging, quantum resilient security, and quantum training.”
    - In the US (Entrust)
        - Has [PQ-enabled HSM operations](https://www.entrust.com/-/media/documentation/datasheets/entrust-pqc-option-pack-ds.pdf?la=en&hash=F5524391F1F9EA203DBEB743CEEC5B65) along with SDK as a advanced preview for current clients
        - Started offering in beta, a [PQ-PKIaaS product](https://go.entrust.com/post-quantum-cryptography?_ga=2.200842606.171189309.1688852905-507437514.1688362737&_gl=1*1g1tmie*_ga*NTA3NDM3NTE0LjE2ODgzNjI3Mzc.*_ga_6QRW66BW5T*MTY4ODg1MjkwNC4zLjEuMTY4ODg1MzI4MS41OS4wLjA.)
        - Also have a center of excellence that acts as an advisory/consultancy for clients to forecast their crypto vulnerabilities and remedy accordingly. More details in their [post-quantum solution page](https://www.entrust.com/solutions/post-quantum-cryptography).
    - In the UK (https://arqit.uk/)
        - They recently [announced a partnership](https://www.globenewswire.com/en/news-release/2022/10/09/2530624/0/en/AUCloud-launch-Australia-s-first-Sovereign-Quantum-Safe-Encryption-Service-powered-by-Arqit-Quantum-Cloud.html) with an Australian company (AUCloud) to power the nation’s first quantum safe encryption service.
        - Does not appear to have penetration in the US and Canada.
        - Has a few services it offers that does not seem to relate? A network adapter, a financial supply chain product to generate and distribute financial contracts, and primarily QuantumCloud - which appears to be their premier offering.
        - Website is kind of bad. No documentation for developers or quick start. Several links to contact them - thinking onboarding process is a lot.
     
## Tech / System Design / Qath Guardian

### An aside (not on Notion)
A summary of Qath's core technology...

Qath's Guardian product is a plug and play solution that developers can integrate into their application to enable end to end post-quantum encryption. It achieves this with a few key components:
- Edge --> This is the service worker a developer would inject into their client side application. This worker intercepts `fetch` events from the site, and if it passes the configuration set by the developer, performs the post-quantum encryption for the outbound request and corresponding decryption for the response.
- Helios --> This is the central server that talks to `Node` and `Edge`. It generates (or fetches) symmetric keys from the public keys of the incoming token, establishes relationships between source and targets, and grants client-side/server-side tokens with an API key.
- Node --> This is the server side middleware component. It has two main roles - (1) decrypts incoming request bodies using the `X-Qath-Identifier` header and encrypts the outgoing response body ; (2) intercepts a token generation request from the client side worker and sends it to Helios to get back a client-side token to return to the worker.

The core technology at work here is the token exchange and symmetric key encapsulation/decapsulation. 

The token exchange is a mechanism built to prevent the API key from being needed in the client worker. The developer configures a custom validation path in the instantiation of the middleware and adds that same path to the configuration of the client worker. When the worker wants to get a symmetric key to perform its encryption duties, it checks the local cache to see if it already has one for the target resource (and that the key refresh time threshold has not been breached). If it cannot find a key, it must talk to `Helios` to acquire one - but it requires a token to do so. To acquire its token, it generates 3 key pairs and sends the public keys to the validation path from its configuration. `Node` then recognizes this validation path (since it is the same as the worker's), and intercepts that request. `Node` fetches the cipher suite configuration (from cache or `Helios`) for its API key and picks the applicable public key. It then sends that public key to `Helios` and asks for a client side token (this call's auth is done via API key). `Helios` then generates a token and sends it back to `Node`. The token is then returned to the `Edge` worker, which can now call `Helios` to generate a symmetric key for a target resource.

The symmetric key encapsulation/decapsulation is fairly straightforward (fundamental PKE), but the open source libraries didn't have APIs to encrypt information using a public key and decrypt information using a private key. The KEM APIs existed which had the basic logic for doing those operations (but only for a specific `byte[]` size) since they would be required to derive a symmetric key, generate its encapsulation and ciphertext, and extract the symmetric key from the cipher text. Special modifications to these libraries were needed to support custom encryption/decryption 'out of the box' for Qath's use case. For C#, it was the following modifications to the BC-CSharp library:

`KyberEngine.cs`
```csharp
internal void MessageEncrypt(byte[] cipherText, byte[] m, byte[] pk)
{
    byte[] randBytes = new byte[SymBytes];
    byte[] buf = new byte[2 * SymBytes];
    byte[] kr = new byte[2 * SymBytes];

    m_random.NextBytes(randBytes, 0, SymBytes);

    Symmetric.Hash_h(randBytes, randBytes, 0);
    Array.Copy(randBytes, 0, buf, 0, SymBytes);

    Symmetric.Hash_h(buf, pk, SymBytes);

    Symmetric.Hash_g(kr, buf);

    m_indCpa.Encrypt(cipherText, m, pk, Arrays.CopyOfRange(kr, SymBytes, 2 * SymBytes));
}

internal void MessageDecrypt(byte[] rawSecret, byte[] cipherText, byte[] secretKey)
{
    m_indCpa.Decrypt(rawSecret, cipherText, secretKey);
}
```

`KyberKEMExtractor.cs`
```csharp
public byte[] DecryptSessionKeyWithPrivateKey(byte[] cipherText)
{
    // raw secret length should be the same as the extracted secret from the encapsulation flow
    byte[] rawSecret = new byte[m_engine.CryptoBytes];
    m_engine.MessageDecrypt(rawSecret, cipherText, ((KyberPrivateKeyParameters)m_key).GetEncoded());
    return rawSecret;
}
```

`KyberKEMGenerator.cs`
```csharp
public byte[] EncryptSessionKeyWithPublicKey(AsymmetricKeyParameter publicKey, byte[] sessionKey)
{
    KyberPublicKeyParameters key = (KyberPublicKeyParameters) publicKey;
    KyberEngine engine = key.Parameters.Engine;
    engine.Init(m_random);

    // m is the shared secret generated via the encapsulation and is guaranteed to not be more than 32 bytes
    // The guarantee is secured by the KyberEngine.CryptoBytes which is set equal to the KyberEngine.SharedSecretBytes which is set as a constant to 32
    // consequently, the cipher text size can be equal to the KyberEngine.CryptoCipherTextBytes as it is done in the encapsulation flow.
    byte[] cipherText = new byte[engine.CryptoCipherTextBytes];
    engine.MessageEncrypt(cipherText, sessionKey, key.GetEncoded());

    return cipherText;
}
```

The JS library modifications can be found in the `Edge` project, under the `patches` folder, but they are very similar to the above. More details are in Notes on Macbook/iOS called `Qath Vault`.

The above modifications and core technology basically allowed plug and play as the developer would only have to inject the worker in their client side app, inject the middleware in their web server, and configure both correctly for everything to work end to end. Now let's get back to the Notion archival...

### Back to Notion Archival (Tech / System Design / Qath Guardian)

**Description**

Qath Guardian is a product suite that enables end to end post-quantum encryption for enterprises with no additional end-user (mobile, web, etc.) installation. 

It is designed from the ground up with zero-trust architecture to enable enterprise-grade cryptographic agility and visibility, and is also quick to deploy on premises or integrate with existing major cloud platform architectures.

Guardian is developed and vetted in conjunction with experts from academia and industry, and is accompanied with robust documentation to keep onboarding and integration as seamless as possible for development teams.

**Features**

- [MVP - **P0**] Agent and proxy servers that are mutually authenticated and create a quantum-secure data tunnel (similar to DRM) through which data can be transmitted over private networks and the open internet.
- [MVP - **P0**] Control plane with cryptographic utilities, access management, and authorization policies
- [MVP - **P1**] Analytics and traffic monitoring to give the client visibility into their network landscape
- [MVP - **P2**] Threat monitoring and pattern analysis

### Tech / System Design / Qath Guardian / Backlog of Compromise

**Bolded points were implemented**

**Technology - Helios**

- **Authentication / Authorization**
    - Add Organizational and User scheme (for onboarding new clients)
    - Add more claims and configurations (per API key level), and construct claims principals based on config values in middleware.
        - **Add special logic to account for front end tokens and add claim checks to prevent any unauthorized use of front-end tokens**
    - Add custom principals/contexts for each type of auth.
        - Definitely make a TokenContext and UserContext that will be constructed from the claims of the authenticated ticket
        - **Back-burner for now^, just parsing out the claims as needed from the Authentication Ticket at the controller layer — this will require some refactoring once the codebase starts to get more complex**
- **Symmetric Partitioning** - making sure only approved sources and targets can create/fetch generated keys
    - Each API key is associated with only one endpoint. This endpoint will be part (as a claim) of the token generated for this API key by the TurnKey service.
    - When the above token is used to generate a symmetric key, a relationship is created between the endpoint from the claim (as a source) and the requested resource from the HTTP body.
        - The relationship will be indexed by the ID of the symmetric key
        - This relationship will have a TTL of the API key’s configured expiry + n minutes (~5)
            - Alternatively, the relationship can have a TTL of the max of the refresh rate of the source and target + n minutes (~5). Ensuring that the key will persist a bit longer than it may be needed.
            - **Even easier of an alternative, set a cap for how long the refresh rate can be (60 minutes), and set the relationship TTL to 121 minutes (chosen for now, can improve later on)**
    - When a symmetric key is requested to be fetched, a similar check will happen to make sure the relationship exists.
        - **The endpoint will be parsed from the requesting token, and a check will be performed to make sure the endpoint is the target resource. This lookup will be performed using the ID of the symmetric key the endpoint received.**
    - In either case (fetch or create), if the key is to be returned - it will be signed with the public key that was onboarded by that token earlier.
    - Some things to note and think about later:
        - Expiry times of the relationship and symmetric key - **default TTL of 65 minutes for each new relationship as highest refresh rate is 60 minutes (can change this later)**
        - Cache/Persistence of the symmetric relationship - saves and reads will be done in really low latency (within a couple seconds), so strong consistency may have to be applied for globally distributed calls
- **Post Quantum TLS - will be a server config (not in codebase as far as I know)**
    - Have to figure out if there is an existing way to enable PQ-TLS on Helios servers. Consider using [AWS s2n](https://github.com/aws/s2n-tls)
    - Chrome recently added [PQ-TLS support on version 116](https://blog.chromium.org/2023/08/protecting-chrome-traffic-with-hybrid.html). This is important because the worker on the front end application does not have the capability to choose the cipher suite. Server side is fine because the developer has the control, but not on the browser 😟
        - The best way to get around this is to keep up with latest news and updates on browser support for front end, and ensure customers are aware that it is a browser-based timeline for guaranteed PQ protection (specifically for front end to server side communication, server to server is still fine).
        - Another problem this presents is the worker’s ability to fetch quantum randomness to generate the key pair. Helios will have an API to deliver a quantum random number, but this API has to be protected by PQ-TLS. This is feasible for server-to-server, but not for the worker since it will be based on browser support. The only way to work around this is to use a built in JS library for random number generation, **if the browser does not support the PQ-TLS ciphers**.
        - The benefit, on the other hand, is that the customer would be able to become quantum resistant as soon as any of their user uses a browser that supports the new cipher schemes.
    - **At time of writing (Sept 6), it’s hard to find out of the box implementations for post quantum TLS http clients in .NET Core. This will have to be implemented by Qath at some point soon, but I have other priorities right now (to get the whole thing working, of course).**
        - That being said, **we still have the mutual encryption/decryption to fall back upon**. To generate a token, it is based on the API key and can be signed with the public key so the token can only be unwrapped the by the holder of the API key.
        - We can mandate API key rotations every so often to make this more secure^
        - Symmetric key generations and fetches are also protected with the mutual encryption/decryption. **Since these key pairs are post-quantum resistant, they can practically work over non-quantum resistant protocols,** with a caveat that the data protected by traditional cipher, if broken, would still be protected by a quantum key pair.
            - Effectively, we don’t have to use the PQ-TLS at time of writing. **But, we absolutely should invest in building out our HTTP/S clients to support it. It will be useful to fetch quantum random numbers, and better security overall**.
- **UI Administrative Dashboard (Config+API Key Management, Users, and Basic Telemetry)**
    - Need some basic capabilities for clients:
        - Add and delete users
            - Roles can come later
        - Add API Keys and configure them (ciphers, etc.)
    - Have some basic telemetry and usage details
        - Later enhancements can be threat detection, traffic patterns, etc.
        - Billing service can leverage this later
- **Data Store Connections / Cloud Services**
    - Need to make resources in cloud platform (likely Azure) and then build out provider connections and get rid of the todos.
- **Quantum Randomness**
    - Can use [AWS solution in Marketplace](https://aws.amazon.com/marketplace/pp/prodview-246kyrfjo3bag)
    - Can also build your own [QRNG using Azure Quantum](https://learn.microsoft.com/en-us/azure/quantum/tutorial-qdk-quantum-random-number-generator)
    - Needs PQ-TLS to be enabled for this to be relevant

**Technology - Front End Agent (JS)**

- AuthN/AuthZ
    - Will have to use a configuration like the one designed before to specify a validation endpoint.
    - Package would call this endpoint with the client token. Client is only responsible for validation the user/service token with their own logic.
    - If it is valid, then client can use our SDK to generate a token with the API key and return it to the caller (the package, in this case, that is passing the user token in).
        - Note - the same SDK can have a different namespace for the middleware component that will be responsible for the encryption and decryption part - although it too will still need access to the API key.
        - Another idea - check if it is possible to use the middleware as the API itself. In other words, have some sort of instantiation parameter for the validation route, that the middleware can intercept. The middleware can also be instantiated with a lambda to verify the token, and the API key to create a Helios token if the validation passes.
- Future Concerns
    - CORS??

**Product**

- Perform academic consult with at least two people (prof & grad student)
- If possible, get cyber security consult
- **At time of writing, the Guardian product will be limited to securing HTTP calls. And specifically, the body segment of the request and response. This means 1/3 parts of the HTTP message is secured (leaving the headers and the request line, [more info on message structure here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages))**
    - It is possible to encrypt the headers as well, but requires more work and learning from clients to see if there is demand.
- If research from potential and current clients shows that the proxy server is suitable (a.k.a, the company trusts us with the private server certificates), then we should migrate away from the middleware component.
    - The problem with the proxy server is that it requires a lot more caution and consideration (affecting load balancing and server architectures already set up by clients)
    - But, it is ‘cleaner’ and makes development + maintenance easier for Qath (instead of supporting several different SDKs/packages that clients would use).

**Deployment**

- Figure out test coverage and pipelines
- Understand publishing of packages and how they can be updated

### Tech / System Design / Qath Guardian / Dev Designs / Token Generation

#### Option 1 - Time of Key Generation

One scenario is that we can designate the public counterpart at time of API Key Generation. It would work something along the lines of that the key pair would be generated client side at time of creating an API key, and we display the private counterpart temporarily and persist the public counterpart in Helios associated with the API key.

However, there are a couple problems:

- Crypto agility - changing the cipher scheme would require a rotation of the private key on the user’s side as well
- Hard and insecure to integrate this functionality into the front end SDK/worker. It would require having a static private key instantiated in the SDK
- Forward secrecy - having a leaked private key would compromise any symmetric key communications between Helios and nodes. However, this would require breaking the PQ-TLS connection, so maybe not a big concern but definitely not good

#### Option 2 - Time of Token Generation

The chosen path is thus the following - **specify the public key at time of token generation**. Effectively, the public key is specified in the token generation request (this is protected by the API key). If the API Key validation passed, then the public key is added as a claim in the generated token.

- Helios would sign any outbound data (keys in this case) with the claim value of the public counterpart present in the token. This would then be able to be decrypted by the holder of the API key.
- In terms of an attack surface, one would need ************either************ (1) the API key, ****or**** (2) the token and the private key. In either case, the user is expected to keep the value(s) private.

**Option 2 Details**

**Server Node**:

1. Middleware instantiated with API key
2. Middleware acquires current configuration using API key
3. Middleware generates key pair based on configured cipher, and acquires a token via API key exchange.
    1. Note - this token exchange must have a body holding the public key from the generated pair on the node
4. Middleware is now ready to generate and fetch symmetric keys from Helios. Once the token expires (based on the refresh rate), a new config would be picked up, a new pair generated, and a new token exchanged
    1. Note - request and response modifications in C# require Stream modifications. See here for an [explainer](https://stackoverflow.com/questions/44498802/asp-net-core-modify-substitute-request-body).

**Service Worker / Front End Node**:

1. Service worker instantiated with validation endpoint and scope (?) of the paths and routes it is supposed to work on
2. If worker does not have a valid token in its cache, then it will call the validation endpoint with a request body containing a set of public keys. This set is needed because the worker does not know the configuration set by the user at time of key pair generation (unlike the middleware, which can fetch the config beforehand with the API key)
    1. If the auth check (by the user) succeeds, then the middleware will check its configuration to see which public key from the set to use. It finds that, and then forwards a special front-end token generation request to Helios.
    2. Helios generates a token for the front-end worker. This token is special in the sense that it does not have the rights to fetch a symmetric key, only to generate. The rationale is that the front end would never really have a reason to fetch symmetric keys since it only dispatches requests and listens for the response.
3. This front-end token is then returned to the service worker. It caches it, and is now able to encrypt requests and decrypt responses

### Tech / System Design / Qath Guardian / Dev Designs / Users, Orgs, and AuthZ

<img width="664" alt="image" src="https://github.com/qathio/qath-docs/assets/134471039/271eac31-633f-4f3c-9e9d-b1e1f60dea5f">

<img width="661" alt="image" src="https://github.com/qathio/qath-docs/assets/134471039/28632915-7892-4695-acea-b74b5d917627">

<img width="414" alt="image" src="https://github.com/qathio/qath-docs/assets/134471039/7f68bd61-c549-48a5-ad88-a349d8a68dd4">

### Tech / System Design / Qath Guardian / Work Items

#### Production Stability

1. Create staging environments (swaps) for UI and Helios, and adjust CI/CD pipelines to deploy there first of course… ✅
2. Add proper telemetry in Helios and pipe to App Insights + add exception middleware
3. Add proper pipelines for Node and Edge and adjust CI/CD pipelines for UI, Node, and Helios to use the deployed bits and minified JS from CDN
    1. For BC-CSharp modification, make Github registry to host drop build and Github action to build and upload to drop (with versioning) ✅ (also added readme to have info on how to sync new commits)
    2. For Node (C#), internalize classes ✅
    3. For Node (C#), pick up drop from BC-CSharp, build, and then publish to open NuGet ✅
    4. Modify Helios API project to have a package reference to NuGet for Node (C#) instead of local DLL ✅
    5. Devise proper versioning system especially for Edge since it is a common component and stack agnostic and modify UI pipeline to pick that up from CDN, download into public directory, and then build + deploy  ✅
4. Remove AES Params from Node and Helios. Shouldn’t change anything but run some tests. ✅

#### Helios

1. Add User registration and control panel APIs after login
2. Add plan hierarchy support from a data layer perspective (only Basic for now, since you can’t charge)
3. Control panel APIs should be relatively simple
    1. Ability to create API keys (2 maximum for now) 
    2. Edit cryptographic controls
    3. Ability to select plan
4. Add RPS system to throttle
    1. Note - this shouldn’t be applied for 

#### Edge

1. Add better error handling 
    1. Config value for enabling always dispatch - aka if encryption cannot be performed, bypass regardless and send request (better for reliability)
    2. Config value for debug - if set to true, debug statements should print (recommend only for developer setting)
2. Investigate Firefox support (if it is actually a problem, maybe it’s just an issue with seeing the worker logs?)

#### UI

1. Fix https://github.com/qathio/qath-ui-next/issues/1 - minor improvements ✅
2. Add UI pages for login and crypto controls, and a section to handle the plan of the current user (only Basic for now, but add disclaimer to email if more premium options are required)
3. Add documentation and quick start. Important to have documentation on error handling.
4. Add UI logging to gather data on site visits and locations, pipe to app insights

#### Node

1. Come up with a generic (language agnostic) way to surface exceptions from middleware to API layer
    1. Can be Helios unexpected errors (HTTP 500s)
    2. Can be expected errors (throttling, key not found)
2. Make custom library for Kyber only operations (backlog this..) and obfuscate the code in the CI process

#### Features

1. Telemetry for Users in Control Panel space
2. Add encryption support for cookies and header values
    1. This might prove to be a bit hard and require a redesign in Node and Edge
  
### Tech / Product / High Level Stages

#### Setup

Although there are many moving parts that accompany such a transition from classical computing to quantum computing, the world moves slow and adoption will have to be done in phases.

The real breakthrough at the moment is the advent of new standardizations of post-quantum secure KEMs and digital signature algorithms. Kyber, the only approved PQC KEM, effectively enables the quantum-secure public key cryptography to exist.

#### Takeaway

So what is the real takeaway here? We can’t expect everyone to switch their production workloads to a new public key cryptographic standard for so many reasons:

- Legacy systems (a lot of systems do not currently support TLS 1.2 let alone 1.3)
- Browser and client support for new/hybrid TLS ciphers - specs take a long time to be negotiated, implemented, tested, and deployed (this is also disregarding the updating on the end-user and developer standards)
- Risk management - new algorithms have not been tested for too long yet, and the standards may change, which discourages current adoption.

All this being said, it is clear to see that there is a lot of value to capture in enabling enterprises to achieve cryptographic agility. Such a charter is already being recommended by the US government (DHS, NSA) and the EU.

- Impending regulation on new cryptographic standards will leave businesses in a state of unpreparedness to secure their corporate, transactional, and user data.
- Impending generally available quantum computing could leave enterprise data (at rest and in transmission) at risk of breach. [IBM’s 2022 Cost of a Data Breach Report](https://www.ibm.com/reports/data-breach) mentions that the average cost of a data breach in the US >$9M, with the global average at >$4M and healthcare average at ~$10M

#### Strategy

From the above point, we know that the proper MVP has to be one that allows the enterprise to achieve post-quantum cryptographic agility without any disruption to their current product or users.

Further, it also has to be quick and seamless to integrate into existing deployment architectures with as minimal as possible setup for the enterprise. It must also give visibility into the crypto utilities in place, along with enhanced features for analysis and threat protection.

Lastly, and almost most crucially, it has to be trustworthy and developer-friendly. Building trust would involve some level of sign-offs (compliance certifications like FedRamp & SOC, third-party vetting by security teams or academic advisors, open-sourcing appropriate modules for transparency). Having developer-friendly resources is pretty self-explanatory here - allows for easier adoption and dev team onboarding.

To summarize, a proper MVP must satisfy:

- Ability to enable cryptographic agility without disruption to production workloads or users.
    - Agility also encompasses visibility of crypto utilities and data traffic / threat patterns
- Seamless and developer friendly integration in existing deployment architectures with minimal client setup
    - On-premises deployment offering for private networks
    - Major cloud platform service offerings via marketplaces
    - Open-source SDKs and thorough documentation
- Build trust via compliance certifications, security audits, and/or open-source modules

#### Product Roadmap

Now that the requirements have been listed very clearly, the following defines the product growth roadmap for Qath.

The overarching vision for this roadmap is inspired by Qath’s mission to be the platform for post-quantum information security. The underlying ideas are that PQC adoption will be relatively slow and will occur in phases.

**First Product - Qath Guardian**

The primary value proposition of this product will be its **low barrier to entry.** 

By virtue of covering the requirements above, Guardian will ensure quick, trustworthy, developer-friendly integration for enterprises to quantum-secure their communications.

**So what is it?** - Guardian is a product suite of proxy agents and servers that are post-quantum enabled. It will allow for quantum-secure communications for server to server and client to server interactions without any additional end-user installation.

**Features**

- [MVP - **P0**] Agent and proxy servers that are mutually authenticated and create a quantum-secure data tunnel (similar to DRM) through which data can be transmitted over private networks and the open internet.
- [MVP - **P0**] Control plane with cryptographic utilities, access management, and authorization policies
- [MVP - **P1**] Analytics and traffic monitoring to give the client visibility into their network landscape
- [MVP - **P2**] Threat monitoring and pattern analysis

[**Disclaimer]** The rest of the product road map is expected to change depending on performance, product market fit, and consumer demand. Nevertheless, putting it down here.

**Second Product - Qath Vault**

The primary value proposition of this product will be its ability to quickly help setup the cryptographic foundation for entities to integrate PQC in their systems.

**So what is it? -** Vault would be a hardware security module (HSM) as a service offering. It would be a cloud based service that enables developers to perform post-quantum cryptographic operation on a compliant hardware device.

- Similar offerings already exist as part of the major cloud providers (Azure Key Vault, AWS KSM, etc.). However, they are not yet enabled to run PQ operations.
- Entrust is an example of offering a preview of their nShield HSMs that are able to run these operations at time of writing. More details in their section in the [Intro](https://www.notion.so/Intro-ce53bdd3cefa4b0f9d8c677e94bfe5bb?pvs=21) page.

**Features**

- Ability to provision and run PQ operations on compatible and FIPS compliant HSM devices

**End Product - Qath PKIaaS**

Lastly, a post-quantum enabled PKIaaS would be the premier offering of Qath. It would require that at least Qath Vault be operational. Consequently, building a PKI product on top of Vault would be a great segue into more vertical integration for the company.

This would involve an organization embracing PQC from the ground up and would involve the longest transition period out of the three products.

However, it would enable a lot of other features based off the enterprise’s PKI. Such features would include:

- Identity (IDaaS)
- Signing (Code, Documents)
- Secure Email
- IoT
- Supply Chains

Out of the above features, IoT seems to be the largest market in context of SNDL attacks as those products often have the longest shelf life and be most exposed.

### Growth / Marketing and Adoption

How can we convince enterprises, and by extension - developers, to use our offering?

- Fundamentally —> A fantastic product, that is easy to use, easy to learn, and satisfies the user’s requirements.

#### In the beginning

- Do things that do not scale - founders will have to recruit users manually, and **learn sales**. We have to want it, otherwise this will never work.
    - Cannot hire a sales team until we know sales ourselves. It will help in understanding the type of clientele we attract and what they are looking for.
    - It helps to know the problem we are solving, and knowing the market really well
    - A love of solving problems goes a long way. Customers will know that you really care.
- Sales funnel
    - Qath will have a largely product-led and outbound sales approach. In other words, the product speaks for itself in terms of its advantage and future compliance. Outbound sales will hopefully help larger conversions.
        - One of the largest mistakes earlier on is not doing enough outbound sales yourself. Each step in the funnel will have some dropouts. It’s hard to know personal strengths in sales until enough data is gathered to know what the dropout rates are
- Pricing
    - Have to charge even, even for the first customer
        - Signalling that Qath is providing something of value to the end user
        - To make it more attractive - can add things like free trial, money back guarantee with time expiry, and opting out of contracts (for larger users)

#### Adoption

- Have migration guides away from major providers such as Okta and other large IDaaS platforms
    - Reasoning —> as regulations and standards become more clear, companies would be forced to adopt PQC. Our goal should be to make the migration as easy and seamless as possible
- Developer friendly documentation
    - Reasoning —> Make it super easy for developers to use us. Stripe was successful because it simplified transactions into one API call.
- Cater to startups specifically - stealing an idea from vendor lock-in, if we can convince nascent companies to use our platform then it is easy to keep them tied to us for life
    - Risk —> higher churn rates as most startups fail

#### Marketing

- SEO - online search does not yield any company that specializes in this area, which means there is space to capture by focusing on “quantum safe encryption” and “PQC” as keywords.
- Have a great demo
- Compliant with requirements from local and federal agencies —> makes for a peace of mind for larger organizations that need compliance certification
- Patents?
    - A enterprise system to handle PQC?
- Go to competitor websites (JumpCloud, SailPoint, Okta) and look at their testimonials. If there is a quoted person, try to find that person’s contact on LinkedIn or other sites and use it for lead generation.

### Product / Launches

There are several different type of launches that can be done:

- **Silent launch** - landing page with company name, one-liner pitch, waitlist button
    - One-liner should be short, descriptive, and meaningful. No marketing jargon, concise and accurate
        - “Qath is the world’s first [quantum-safe || quantum-resistant || post-quantum cryptography] identity as a service platform”
- **Friends and family launch** - tell friends and family about the product, and get initial feedback on one-liner.
    - Not advisable to stay in this launch for too long since they might not be ideal users of the product.
    - Good way to leverage social connections and get people to talk about you (even if for a short time)
- **Stranger launch** - tell others about the product through different avenues (even under guise if need be), and get feedback
- **Online community launch / social media launch** - great thing about IDaaS is that developers are bound to use it. Great onboarding experience can help with signups and prevent churn in the long run. Be engaged and authentic in these types of launches.
    - HackerNews
    - If in YC - then BookFace
    - Dev forums
- **Request access launch** - this is fairly straightforward. Best to do it once a MVP is set up along with documentation and contact support channels.
    - Don’t wait too long doing this - harder to convert people as time goes on since they may forget or lose interest
- **Press launch** - only relevant if big funding round or big investor joins the scene
    - Not a silver bullet - cannot count on it to achieve product market fit
 
### Product / Compliance

Qath will be a platform level company, where the underlying technology is appealing to a wide range of industries that will likely have a range of compliance requirements.

**At the top level, we always have to ensure we remain compliant with NIST’s standards for PQC.**

I asked GPT-4 to help me with this: “*Are there any compliance certifications that will be useful in client acquisition or conversion? Since PKI is a platform level offering, this will appeal to a wide range of industries that might have specific regulations regarding data transfer and storage*”

Answer:

Compliance certifications can indeed help build trust with potential clients and improve client acquisition or conversion. Since PKI is a platform-level offering, having certifications that demonstrate your adherence to various regulations can be beneficial. Some important compliance certifications and frameworks relevant to PKI include:

1. **WebTrust for Certification Authorities**:
WebTrust is an auditing and assurance program for Certification Authorities. Compliance with WebTrust principles ensures that your CA operates with transparency, security, and integrity. Acquiring a WebTrust Seal can build trust with clients who rely on your PKI services.
2. **ISO/IEC 27001**:
ISO/IEC 27001 is an internationally recognized standard for information security management systems (ISMS). It demonstrates your organization's commitment to implementing and maintaining a robust security framework to protect sensitive data, including the management of cryptographic keys and certificates.
3. **SOC 2**:
Service Organization Control (SOC) 2 is an auditing procedure that ensures service providers securely manage customer data to protect its privacy and confidentiality. SOC 2 compliance demonstrates your PKI platform's adherence to security, availability, processing integrity, confidentiality, and privacy principles.
4. **GDPR**:
The General Data Protection Regulation (GDPR) is a European Union regulation that focuses on data protection and privacy for individuals within the EU. Ensuring your PKI platform complies with GDPR is essential if you plan to serve clients who process personal data of EU citizens.
5. **HIPAA**:
The Health Insurance Portability and Accountability Act (HIPAA) is a US regulation that establishes requirements for the use, disclosure, and safeguarding of protected health information (PHI). If your PKI platform targets clients in the healthcare industry, compliance with HIPAA is crucial.
6. **PCI DSS**:
The Payment Card Industry Data Security Standard (PCI DSS) is a set of security standards designed to ensure that all companies that accept, process, store, or transmit credit card information maintain a secure environment. Compliance with PCI DSS is essential if your PKI platform serves clients who handle payment card data.
7. **FIPS 140-2/3**:
The Federal Information Processing Standard (FIPS) 140-2/3 is a US government standard that defines security requirements for cryptographic modules. Compliance with FIPS 140-2/3 demonstrates that your PKI platform uses secure cryptographic modules to protect sensitive data.

### Learning Resources

General:

- [MSR’s PQC](https://www.microsoft.com/en-us/research/project/post-quantum-cryptography/](https://www.microsoft.com/en-us/research/project/post-quantum-cryptography/)) efforts
- [Alibaba](https://www.alibabacloud.com/knowledge/tech/quantum-safe-cryptography) explainer on PQC

Startups:

- [Slidebean](https://www.youtube.com/@slidebean) - good channel to learn about startup funding and economics, along with case studies. Also has several resources useful for startups.
- [Garry Tan](https://www.youtube.com/@GarryTan) - newly minted head of YCombinator. Very early engineer at Palantir. Funded Coinbase and several other unicorns. Makes a lot of videos for founders

Accelerators

- YC
    - [What they look for in applications](https://www.youtube.com/watch?v=-iNjpJ52i8s&ab_channel=YCombinator)
        - What and why of the product
        - Why the team
        - How far along
    - Startup School [playlist](https://www.youtube.com/playlist?list=PLQ-uHSnFig5M9fW16o2l35jrfdsxGknNB)

PQC Risk Assessments

- Entrust Post Quantum [self assessment](https://go.entrust.com/pq-self-assessment?_ga=2.130201807.171189309.1688852905-507437514.1688362737&_gl=1*1xopkwh*_ga*NTA3NDM3NTE0LjE2ODgzNjI3Mzc.*_ga_6QRW66BW5T*MTY4ODg1MjkwNC4zLjEuMTY4ODg1MzAwOS42MC4wLjA.)
- Wells Fargo Risk Model - https://www.fsisac.com/hubfs/Knowledge/PQC/RiskModel.pdf
- https://www.fsisac.com/hubfs/Knowledge/PQC/InfrastructureInventory.pdf
- IBM Roadmap - https://research.ibm.com/blog/quantum-safe-roadmap
    - Quantum TLS Documentation - https://cloud.ibm.com/docs/key-protect?topic=key-protect-quantum-safe-cryptography-tls-introduction

<img width="1180" alt="image" src="https://github.com/qathio/qath-docs/assets/134471039/414bf0d6-c6c4-45c7-bdc1-2de453e3923e">

Vision 2.0 References:

- [VMWare’s take](https://octo.vmware.com/cryptographic-agility-exploring-proxy-approaches/) on exploring proxy servers for cryptographic agility
- [QuProtect](https://www.qusecure.com/quprotect/) - zero client side (browser, device, IoT, etc) install quantum safe sessions + backend server to server quantum safe communications.
    - Uses FIPS certified quantum pseudo random number generator
    - Control plane visibility + user’s option for level of security and selection of algorithms
    - Claim they are quick to deploy with no client side installs
    - Case Studies:
        - [QuEverywhere Jan 2023](https://www.qusecure.com/wp-content/uploads/2023/01/QuSecure-Case-Study-QuEverywhere.pdf)
        - [QuEverywhere June 2023](https://www.qusecure.com/wp-content/uploads/2023/06/QuSecure-QuProtect-QuEverywhere-June-2023.pdf)
        - [QuNetwork Server to Server June 2023](https://www.qusecure.com/wp-content/uploads/2023/06/QuSecure-QuProtect-QuNetwork-June-2023.pdf)
    - [Webinar]([url](https://www.youtube.com/watch?v=RTrAhg5ErHM&list=PL9WeYZh1Eq3E5tEb8WKVWmz4GD4kVYseS&index=13&ab_channel=QuSecure)https://www.youtube.com/watch?v=RTrAhg5ErHM&list=PL9WeYZh1Eq3E5tEb8WKVWmz4GD4kVYseS&index=13&ab_channel=QuSecure) - High Level diagrams around after 30 minute mark ; latency and solution description at 53 minute mark

<img width="1205" alt="image" src="https://github.com/qathio/qath-docs/assets/134471039/5a3b480c-4481-401d-bd26-07ba5da3c6d3">

<img width="1212" alt="image" src="https://github.com/qathio/qath-docs/assets/134471039/4ba59875-6999-49b6-87f7-f8d7bc340370">

Advanced Engineering References:

- [SSO and IAM](https://jumpcloud.com/blog/sso-isnt-identity-management)
- [Swoosh](https://eprint.iacr.org/2023/271.pdf) - Lattice based NIKE (non interactive key exchange)
- [Post Quantum Diffie-Hellman](https://csrc.nist.gov/CSRC/media/Events/Second-PQC-Standardization-Conference/documents/accepted-papers/soukharev-pqdh-paper.pdf) exchange
- [Hybrid Encryption](https://neilmadden.blog/2021/01/22/hybrid-encryption-and-the-kem-dem-paradigm/) (KEM/DEM) & [Authenticated + Multi-Recipient KEM](https://neilmadden.blog/2021/02/16/when-a-kem-is-not-enough/)
- [CloudFlare PQ-KEM](https://blog.cloudflare.com/post-quantum-key-encapsulation/) algorithm
- [CloudFlare ECC](https://blog.cloudflare.com/a-relatively-easy-to-understand-primer-on-elliptic-curve-cryptography/) explainer
- [EJBCA CE SQL](https://github.com/Keyfactor/ejbca-ce/blob/main/doc/sql-scripts) setups

Other:

- [PQC Initiative](https://www.cisa.gov/quantum) by CISA - good starting point to look at the initiative and the strategy it is taking
- [NIST Selected Algorithms for 2022](https://csrc.nist.gov/Projects/post-quantum-cryptography/selected-algorithms-2022)

### Budget

Budget: $10,000 USD

Expenses:

Domain - $100 CAD

GPT-4: $20/month since May

Proton Mail - $8/month since Sept 23

Dall-E - 115 credits / $15 (Sept 28)

Azure Spend - Credentials in `Qath Vault` in Notes (iOS/Macbook)

Nov 9 - $176.64 - [Azure Link](https://portal.azure.com/#view/Microsoft_Azure_GTM/InvoiceDetailsBlade/invoiceId/G032359073/scopeId/%2Fproviders%2FMicrosoft.Billing%2FbillingAccounts%2F0c5458e6-94ab-5426-f223-7863d1cf0767%3Afca57e15-9617-418c-8b88-8273b65ab3ab_2019-05-31%2Finvoices%2FG032359073/invoicePeriodStartDate/2023-10-01T00%3A00%3A00.0000000Z/invoicePeriodEndDate/2023-10-31T23%3A59%3A59.9999999Z)

Dec 9 - $398.12 - [Azure Link](https://portal.azure.com/#view/Microsoft_Azure_GTM/InvoiceDetailsBlade/invoiceId/G034129689/scopeId/%2Fproviders%2FMicrosoft.Billing%2FbillingAccounts%2F0c5458e6-94ab-5426-f223-7863d1cf0767%3Afca57e15-9617-418c-8b88-8273b65ab3ab_2019-05-31%2Finvoices%2FG034129689/invoicePeriodStartDate/2023-11-01T00%3A00%3A00.0000000Z/invoicePeriodEndDate/2023-11-30T23%3A59%3A59.9999999Z)

Jan 9 - $410.42 - [Azure Link](https://portal.azure.com/#view/Microsoft_Azure_GTM/InvoiceDetailsBlade/invoiceId/G036256278/scopeId/%2Fproviders%2FMicrosoft.Billing%2FbillingAccounts%2F0c5458e6-94ab-5426-f223-7863d1cf0767%3Afca57e15-9617-418c-8b88-8273b65ab3ab_2019-05-31%2Finvoices%2FG036256278/invoicePeriodStartDate/2023-12-01T00%3A00%3A00.0000000Z/invoicePeriodEndDate/2023-12-31T23%3A59%3A59.9999999Z)
