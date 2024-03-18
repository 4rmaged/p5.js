# योगदानकर्ता दिशानिर्देश

योगदानकर्ता दिशानिर्देशों में आपका स्वागत है! यह दस्तावेज़ उन नए योगदानकर्ताओं के लिए है जो p5.js में कोड का योगदान करना चाहते हैं, ऐसे योगदानकर्ता जो कुछ तकनीकी चरणों पर अपनी यादें ताज़ा करना चाहते हैं, या p5.js में कोड योगदान के साथ कुछ और करना चाहते हैं।

यदि आप p5.js रिपॉजिटरी के बाहर योगदान करना चाहते हैं (ट्यूटोरियल लिखना, कक्षाओं की योजना बनाना, कार्यक्रमों का आयोजन करना), तो कृपया इसके बजाय अन्य प्रासंगिक पृष्ठों पर एक नज़र डालें। प्रबंधकों या अनुरक्षकों को समस्याएँ की समीक्षा करने और अनुरोधों को खींचने के संबंध में [कार्यपालिका दिशानिर्देश](https://github.com/processing/p5.js/blob/main/contributor_docs/steward_guidelines.md) अधिक उपयोगी लग सकते हैं।

यह अपेक्षाकृत लंबा और व्यापक दस्तावेज़ है लेकिन हम सभी चरणों और बिंदुओं को यथासंभव स्पष्ट रूप से इंगित करने का प्रयास करेंगे। अपने लिए प्रासंगिक अनुभाग ढूंढने के लिए विषय-सूची का उपयोग करें। यदि अनुभाग आपके नियोजित योगदान के लिए प्रासंगिक नहीं हैं, तो बेझिझक उन्हें छोड़ दें।

**यदि आप एक नए योगदानकर्ता हैं, तो आप पहले खंड, "सभी समस्याएँ के बारे में" से शुरुआत करना चाहेंगे। यदि आप विकास प्रक्रिया का चरण-दर-चरण सेटअप चाहते हैं, तो आप "डेवलपर्स के लिए त्वरित शुरुआत करें" अनुभाग देख सकते हैं.**


# Table of Contents

- [All about issues](#all-about-issues)
  - [What are issues?](#what-are-issues)
  - [Issue templates](#issue-templates)
    - [Found a bug](#found-a-bug)
    - [Existing Feature Enhancement](#existing-feature-enhancement)
    - [New Feature Request](#new-feature-request)
    - [Discussion](#discussion)
- [Working on p5.js codebase](#working-on-the-p5js-codebase)
  - [Quick Get Started For Developers](#quick-get-started-for-developers)
  - [Using the Github edit functionality](#using-the-github-edit-functionality)
  - [Forking p5.js and working from your fork](#forking-p5js-and-working-from-your-fork)
    - [Using Github Desktop](#using-github-desktop)
    - [Using the git command line interface](#using-the-git-command-line-interface)
  - [Codebase breakdown](#codebase-breakdown)
  - [Build setup](#build-setup)
  - [Git workflow](#git-workflow)
    - [Source code](#source-code)
    - [Unit tests](#unit-tests)
    - [Inline documentation](#inline-documentation)
    - [Internationalization](https://github.com/processing/p5.js/blob/main/contributor_docs/contributor_guidelines.md#internationalization)
    - [Accessibility](#accessibility)
  - [Code standard](#code-standard)
  - [Software Design principles](#software-design-principles)
- [Pull requests](#pull-requests)
  - [Creating a pull request](#creating-a-pull-request)
    - [Pull request information](#pull-request-information)
    - [Title](#title)
    - [Resolves](#resolves)
    - [Changes](#changes)
    - [Screenshots of the change](#screenshots-of-the-change)
    - [PR Checklist](#pr-checklist)
    - [Rebase and resolve conflicts](#rebase-and-resolve-conflicts)
  - [Discuss and amend](#discuss-and-amend)

---


# समस्याएँ के बारे में सब कुछ

p5.js के गिटहब रिपॉजिटरी (संक्षेप में रेपो) पर अधिकांश गतिविधि समस्याएँ में होती है, जो आपकी योगदान यात्रा शुरू करने के लिए एक शानदार जगह है।


## समस्याएँ क्या हैं?

![p5.js लाइब्रेरी GitHub रिपॉजिटरी का एक क्रॉप्ड स्क्रीनशॉट, केवल ऊपरी दाएं कोने की सामग्री दिखा रहा है। स्क्रीनशॉट के शीर्ष पर मुद्दे टैब के आसपास एक लाल बॉक्स बनाया गया है।](../images/issues-tab.png)

"समस्या" GitHub पर एक पोस्ट के लिए एक सामान्य नाम है जो किसी समस्या को वर्णित करने का उद्देश्य रखता है। यह समस्या एक बग रिपोर्ट, नई फीचर जोड़ने का अनुरोध, एक चर्चा, या p5.js पुस्तकालय विकास से संबंधित किसी भी पोस्ट के रूप में काम कर सकती है। प्रत्येक समस्या के नीचे किसी भी GitHub खाते वाले व्यक्ति, सहित बॉट्स, द्वारा टिप्पणियाँ जोड़ी जा सकती हैं! यह वह स्थान है जहां योगदानकर्ताओं ने परियोजना के विकास से संबंधित विषयों पर चर्चा करते हैं।

जबकि एक समस्या कई विभिन्न कारणों के लिए खोली जा सकती है, हम आमतौर पर केवल p5.js स्रोत कोड के विकास पर चर्चा करने के लिए समस्याएँ का उपयोग करते हैं। अपने कोड की डीबगिंग, अपने परियोजना में सहयोगी निमंत्रण करने, या अन्य असंबंधित विषयों जैसे विषयों पर हम केवल [फोरम](https://discourse.processing.com) या अन्य प्लेटफ़ॉर्मों जैसे [डिस्कोर्ड](https://discord.gg/SHQ8dH25r9) पर चर्चा करते हैं।

हमने आपको GitHub समस्या होनी चाहिए या कहीं और पोस्ट करनी चाहिए को निर्धारित करने में मदद करने के लिए आसान-से-उपयोग निर्देशिका बनाई हैं!


## समस्या खाका

p5.js के समस्या टेम्पलेट उपाध्यक्षों और रखरखावकर्ताओं को समस्याओं को समझने और समीक्षा करने में सुविधा प्रदान करते हैं। ये आपको भी उचित समस्या को दर्ज करने और त्वरित उत्तर प्राप्त करने में सहायक होते हैं।

![GitHub पर एक मामले की जैसे दिखने वाली एक उदाहरण स्क्रीनशॉट। स्क्रीनशॉट में मुद्दे का शीर्षक "सफारी में चेतावनी लॉग हो रही है जब 2डी मोड में फ़िल्टर शेडर का उपयोग किया जाता है #6597" है।](../images/github-issue.png)

नई समस्या दर्ज करने के लिए, पहले "Issues" टैब पर जाएं पी5.js रेपो पर और फिर दाएं ओर "New issue" बटन पर क्लिक करें। आपको कई विभिन्न विकल्पों के साथ प्रस्तुत किया जाएगा, जिसमें से प्रत्येक किसी संबंधित समस्या टेम्पलेट का अनुसरण करता है या आपको आपके प्रश्न को दर्ज करने के लिए उचित स्थान पर पुनःनिर्देशित करता है। हम सुझाव देते हैं कि आप प्रस्तुत किए गए सभी विकल्पों में से सबसे संबंधित विकल्प का चयन करें ताकि आपकी समस्या को सही ध्यान और समय से संबोधित किया जा सके।

![हरे "नए अंक" बटन के साथ GitHub रिपॉजिटरी के अंक पृष्ठ का क्रॉप किया गया स्क्रीनशॉट, जिसके चारों ओर एक लाल बॉक्स हाइलाइट किया गया है।](../images/new-issue.png)


### ["एक त्रुटि मिला"](https://github.com/processing/p5.js/issues/new?assignees=\&labels=Bug\&projects=\&template=found-a-bug.yml)

जब आप p5.js में संभावित गलत व्यवहार का सामना करते हैं या दस्तावेज़ में वर्णित अनुसार व्यवहार नहीं करते हैं, तो [इस टेम्पलेट](https://github.com/processing/p5.js/issues/new?assignees=\&labels=Bug\&projects=\&template=found-a-bug.yml). कृपया ध्यान दें कि यदि आप अपने स्केच को डीबग करने का प्रयास कर रहे हैं और आपको लगता है कि यह आपके कोड में कोई समस्या हो सकती है, तो आपको पहले [डिस्कोर्स फोरम](https://discourse.processing.org) पर पूछना चाहिए।

इस टेम्पलेट में आपको भरने के लिए कुछ फ़ील्ड हैं:

1. *p5.js का सबसे उपयुक्त उप-क्षेत्र?* - यह हमें संबंधित [लेबल](https://github.com/processing/p5.js/blob/main/contributor_docs/issue_labels.md) के साथ समस्या को स्वचालित रूप से टैग करके आपकी समस्या को पहचानने और उसका जवाब देने में मदद करता है।
2. *p5.js संस्करण* - आप p5.js संस्करण संख्या या तो `<script>` टैग लिंक में या p5.js/p5.min.js फ़ाइल की पहली पंक्ति में पा सकते हैं। यह कुछ हद तक `1.4.2` (अवधि द्वारा अलग की गई तीन संख्याएँ) जैसा दिखेगा।
3. *वेब ब्राउज़र और संस्करण* - यह हमें ब्राउज़रों के बीच विभिन्न व्यवहारों को अलग करने में मदद करता है। ब्राउज़र संस्करण संख्या खोजने के लिए, आप जिस ब्राउज़र का उपयोग कर रहे हैं उसके लिए नीचे दी गई तालिका में दिए गए निर्देशों का पालन करें।

<table>

<tr>

<td>

क्रोम

</td>

<td>

फ़ायरफ़ॉक्स

</td>

<td>

सफारी

</td>

</tr>

<tr>

<td>

पता बार में, `chrome://version` पर नेविगेट करें

</td>

<td>

पता बार में, `about:support` पर नेविगेट करें

</td>

<td>

शीर्ष पट्टी के नीचे “Safari” मेनू में से, “About Safari” का चयन करें

</td>

</tr>

</table>


4. *ऑपरेटिंग सिस्टम* - यदि संभव हो तो आपको ओएस संस्करण संख्या शामिल करनी चाहिए, उदाहरण के लिए, `macOS 12.5`। कुछ बग OS व्यवहार से उत्पन्न हो सकते हैं।
5. *इसे पुन: प्रस्तुत करने के चरण* - यह संभवतः साझा करने के लिए सबसे महत्वपूर्ण जानकारी है। आप जो बग देख रहे हैं उसकी प्रतिकृति बनाने के लिए आपको विस्तृत चरणों की सूची बनानी चाहिए। एक बुनियादी नमूना कोड साझा करना जो समस्या को प्रदर्शित करता है, उस व्यक्ति के लिए बहुत मददगार साबित हो सकता है जो उस बग को दोहराना चाहता है जिसका आप सामना कर रहे हैं और समाधान तैयार करना शुरू कर सकते हैं।

**प्रतिकृति कुंजी है!** इस टेम्पलेट में कई फ़ील्ड का उद्देश्य बग की प्रतिलिपि बनाना है। जितनी अधिक जानकारी आप हमें अपने स्केच के परिवेश के बारे में प्रदान कर सकते हैं और जो आप देख रहे हैं उसे दूसरे कैसे दोहरा सकते हैं, किसी के लिए भी आपकी समस्या को समझना और समाधान खोजना शुरू करना उतना ही आसान होगा।

**जितना संभव हो उतना विस्तृत रहें और सामान्य कथनों से बचें**, उदाहरण के लिए, यह न कहें कि "छवि() फ़ंक्शन काम नहीं करता है" बल्कि अधिक विशिष्ट रहें, जैसे कि "छवि() फ़ंक्शन लोड की गई GIF छवि को प्रदर्शित नहीं करता है सही आकार।" आप जिस बग का सामना कर रहे हैं उसका वर्णन करने का एक उपयोगी तरीका दो चीजों का वर्णन करना है:

1. आपके द्वारा साझा किए गए नमूना कोड से आप क्या अपेक्षा करते हैं (अपेक्षित व्यवहार)।
2. नमूना कोड वास्तव में क्या कर रहा है (वास्तविक व्यवहार)।

यदि आप अभी रिपोर्ट की गई बग को ठीक करने में योगदान देना चाहते हैं, तो आप विवरण में इसका संकेत दे सकते हैं। आप एक सरल सुझाव दे सकते हैं कि आप अभी बताए गए बग को कैसे ठीक करेंगे, इससे हमें पता चलेगा कि समाधान में योगदान देने के लिए आपको कितने समर्थन की आवश्यकता हो सकती है।

**आपको संबंधित मुद्दे के बिना या कार्यान्वयन के लिए किसी मुद्दे को मंजूरी मिलने से पहले पुल अनुरोध दर्ज नहीं करना चाहिए (या कोड परिवर्तनों पर काम करना शुरू नहीं करना चाहिए)**; ऐसा इसलिए है क्योंकि प्रस्तावित सुधार को स्वीकार नहीं किया जा सकता है, पूरी तरह से एक अलग दृष्टिकोण की आवश्यकता है, या वास्तविक समस्या कहीं और है। समस्या को ठीक करने के लिए मंजूरी मिलने से पहले दायर किए गए किसी भी पुल अनुरोध को समस्या को मंजूरी मिलने तक बंद कर दिया जाएगा।

बग रिपोर्ट को ठीक करने के लिए स्वीकार करने के लिए, पुल अनुरोध पर काम शुरू करने से पहले उन्हें कम से कम एक [क्षेत्र प्रबंधक या रखरखाव] (https://github.com/processing/p5.js#stewards) द्वारा अनुमोदित किया जाना चाहिए।


### ["मौजूदा फ़ीचर एन्हांसमेंट"](https://github.com/processing/p5.js/issues/new?assignees=\&labels=Enhancement\&projects=\&template=current-feature-enhancement.yml)

यदि आप परिवर्तनों का प्रस्ताव करना चाहते हैं या p5.js की मौजूदा सुविधाओं (फ़ंक्शन, स्थिरांक, रेंडरिंग, आदि) में कार्यक्षमता जोड़ना चाहते हैं तो इस टेम्पलेट का उपयोग किया जाना चाहिए। उदाहरण के लिए, यदि आप `रंग()' फ़ंक्शन और रंगों को स्वीकार करने वाले अन्य फ़ंक्शन में रंग को परिभाषित करने का एक नया तरीका जोड़ना चाहते हैं, तो यह उपयोग करने के लिए टेम्पलेट है।

इस टेम्पलेट के लिए कुछ फ़ील्ड हैं जिन्हें आपको भरना चाहिए।

1. *एक्सेस बढ़ाना* - यह आवश्यक फ़ील्ड वह है जहां आप एक विवरण डालते हैं कि प्रस्तावित फीचर एन्हांसमेंट को जोड़ने से p5.js को कैसे मदद मिलेगी [एक्सेस बढ़ाएं](https://github.com/processing/p5.js/blob/main /contributor_docs/access.md) रचनात्मक कला या प्रौद्योगिकी के क्षेत्र में ऐतिहासिक रूप से हाशिए पर रहे लोगों के लिए। **इसके बिना कोई प्रस्ताव स्वीकार नहीं किया जाएगा**, हालांकि आप "सुनिश्चित नहीं" भर सकते हैं और समुदाय के अन्य सदस्यों को यह तर्क प्रदान करने की पेशकश कर सकते हैं यदि वे सोच सकते हैं कि यह पी5.जेएस की पहुंच को कैसे संबोधित करता है।
2. *p5.js का सबसे उपयुक्त उप-क्षेत्र?* - इससे हमें आपकी समस्या को पहचानने और उसका जवाब देने में मदद मिलती है। यह स्वचालित रूप से समस्या को प्रासंगिक [लेबल](https://github.com/processing/p5.js/blob/main/contributor_docs/issue_labels.md) के साथ टैग कर देगा।
3. *सुविधा वृद्धि विवरण* - यह वह जगह है जहां आप सुविधा वृद्धि के लिए अपने प्रस्ताव का वर्णन करते हैं। एक अच्छे फीचर एन्हांसमेंट प्रस्ताव में अक्सर एक स्पष्ट उपयोग का मामला शामिल होता है: क्या, कब, कैसे और क्यों इस फीचर एन्हांसमेंट की आवश्यकता है।

फीचर एन्हांसमेंट प्रस्तावों को स्वीकार करने के लिए पुल अनुरोध पर काम शुरू करने से पहले उन्हें कम से कम 1 [क्षेत्र प्रबंधक या रखरखाव] (https://github.com/processing/p5.js#stewards) द्वारा अनुमोदित किया जाना चाहिए।

**आपको संबंधित मुद्दे के बिना या कार्यान्वयन के लिए किसी मुद्दे को मंजूरी मिलने से पहले पुल अनुरोध दर्ज नहीं करना चाहिए (या कोड परिवर्तनों पर काम करना शुरू नहीं करना चाहिए), क्योंकि इस बात की कोई गारंटी नहीं है कि प्रस्ताव स्वीकार कर लिया जाएगा। किसी प्रस्ताव को मंजूरी मिलने से पहले दायर किया गया कोई भी पुल अनुरोध मुद्दे को मंजूरी मिलने तक बंद कर दिया जाएगा।


### ["नई सुविधा का अनुरोध"](https://github.com/processing/p5.js/issues/new?assignees=\&labels=Feature+Request\&projects=\&template=feature-request.yml)

यदि आप p5.js में जोड़ने के लिए एक नई सुविधा का प्रस्ताव करना चाहते हैं तो इस टेम्पलेट का उपयोग किया जाना चाहिए। उदाहरण के लिए एक नए `createTable` फ़ंक्शन के साथ मूल HTML `<table>` तत्वों को चित्रित करने के लिए समर्थन जोड़ना। कुछ प्रस्ताव मौजूदा फीचर एन्हांसमेंट प्रस्तावों के साथ ओवरलैप हो सकते हैं, इन मामलों में आपको बस वही टेम्पलेट चुनना चाहिए जो आपको सबसे उपयुक्त लगे।

तदनुसार, टेम्प्लेट फॉर्म फ़ील्ड "मौजूदा फ़ीचर एन्हांसमेंट" के फ़ील्ड के लगभग समान हैं। अतः कृपया प्रत्येक फ़ील्ड को भरने के तरीके के बारे में विवरण के लिए [पिछला अनुभाग] (#मौजूदा-सुविधा-संवर्द्धन) देखें।

नए फीचर अनुरोध प्रस्तावों को स्वीकार करने के लिए, पुल अनुरोध पर काम शुरू करने से पहले उन्हें कम से कम 2 [क्षेत्र प्रबंधकों या अनुरक्षकों](https://github.com/processing/p5.js#stewards) द्वारा अनुमोदित किया जाना चाहिए।

**आपको संबंधित मुद्दे के बिना या किसी मुद्दे को कार्यान्वयन के लिए अनुमोदित किए जाने से पहले पुल अनुरोध दर्ज नहीं करना चाहिए (या कोड परिवर्तनों पर काम करना शुरू नहीं करना चाहिए), ऐसा इसलिए है क्योंकि इस बात की कोई गारंटी नहीं है कि प्रस्ताव स्वीकार कर लिया जाएगा। किसी प्रस्ताव को मंजूरी मिलने से पहले दायर किया गया कोई भी पुल अनुरोध मुद्दे को मंजूरी मिलने तक बंद कर दिया जाएगा।


### ["चर्चा"](https://github.com/processing/p5.js/issues/new?assignees=\&labels=Discussion\&projects=\&template=discussion.yml)

इस टेम्पलेट का उपयोग तब किया जाता है जब आप जो मुद्दा दाखिल कर रहे हैं वह किसी भी तरह से उपरोक्त में से किसी में फिट नहीं बैठता है। उपरोक्त किसी भी टेम्पलेट में फिट न होने वाला मुद्दा व्यवहार में अपेक्षाकृत दुर्लभ होना चाहिए। उदाहरण के लिए, p5.js में एक विशिष्ट वेब एपीआई सुविधा को अपनाने के बारे में चर्चा को [नई सुविधा अनुरोध](https://github.com/processing/p5.js/blob/main/contributor_docs/contributor_guidelines.md#new-feature-request); विभिन्न रंग कार्यों में एक अतिरिक्त रंग मोड जोड़ने के बारे में चर्चा को [फीचर एन्हांसमेंट](https://github.com/processing/p5.js/blob/main/contributor_docs/contributor_guidelines.md#existing-feature-enchancement); आपके द्वारा आयोजित किए जा रहे स्थानीय रचनात्मक कोडिंग कार्यक्रम के बारे में एक घोषणा मंच पर पोस्ट की जानी चाहिए और यदि आप समर्थन या प्रचार की तलाश में हैं तो प्रोसेसिंग फाउंडेशन से संपर्क करें; वगैरह।

किसी चर्चा मुद्दे को खोलते समय, आप अतिरिक्त प्रासंगिक लेबल जोड़ने के लिए साइड पैनल पर "लेबल" पैनल का उपयोग कर सकते हैं ताकि आप अपने मुद्दे को संबंधित क्षेत्र में साइनपोस्ट कर सकें। टेम्प्लेट स्वयं न्यूनतम पाठ फ़ील्ड है। उदाहरण चर्चा मुद्दे के लिए आप [यह लिंक](https://github.com/processing/p5.js/issues/6517) देख सकते हैं।

[**⬆ शीर्ष पर वापस**](#योगदानकर्ता-दिशानिर्देश)

---


# p5.js कोडबेस पर कार्य करना

## पूर्वावश्यकताएँ

आगे बढ़ने के लिए आपको कमांड लाइन, गिट, नोड.जेएस (कम से कम v18 और ऊपर) के साथ काम करने से न्यूनतम परिचित होना चाहिए, और एक स्थानीय विकास पर्यावरण सेटअप होना चाहिए।


## परिचय

अब जब आपके मुद्दे पर चर्चा हो चुकी है, कार्यान्वयन स्वीकृत हो गया है, और आप कोड में बदलाव करने के इच्छुक हैं, तो आप कोडबेस पर काम शुरू करने के लिए तैयार हैं।

इसी तरह, यदि आपके सामने कोई मुद्दा आया है या आप किसी मुद्दे पर चर्चा में शामिल हुए हैं और कार्यान्वयन को प्रबंधकों द्वारा अनुमोदित किया गया है, लेकिन न तो मूल मुद्दे के लेखक और न ही समुदाय के अन्य सदस्यों ने संकेत दिया है कि वे इस मुद्दे पर काम करने के इच्छुक हैं, तो आप ऐसा कर सकते हैं। यहां योगदान देने के लिए स्वयंसेवा करें और प्रबंधकों से इस मुद्दे को आपको सौंपने के लिए कहें।

**आपको किसी ऐसे मुद्दे के लिए पीआर दाखिल करके "कतार में नहीं कूदना चाहिए"** जिसमें या तो किसी और ने योगदान जमा करने की इच्छा का संकेत दिया है या पहले से ही किसी और को सौंपा गया है। किसी मुद्दे के लिए कोड योगदान स्वीकार करने के लिए हम हमेशा "पहले सौंपे, पहले पाएँ" आदेश को प्राथमिकता देंगे।

यदि आप किसी मुद्दे के लिए पीआर दाखिल करते हैं जबकि कोई अन्य व्यक्ति अभी भी उसी मुद्दे पर काम कर रहा है, तो आपका पीआर बंद कर दिया जाएगा। यदि आप देखते हैं कि किसी निर्दिष्ट व्यक्ति के साथ किसी मुद्दे पर अंतिम गतिविधि को कुछ महीने हो गए हैं, तो आप प्रगति के बारे में पूछते हुए और यदि उन्हें कार्यान्वयन में सहायता की आवश्यकता है, तो उस मुद्दे पर एक विनम्र टिप्पणी छोड़ कर उनके साथ जांच कर सकते हैं। हम आम तौर पर लोगों को उनके योगदान पर काम करने के लिए उचित रूप से लंबी समय सीमा की अनुमति देते हैं क्योंकि हम समझते हैं कि ज्यादातर लोग अक्सर स्वैच्छिक आधार पर काम करेंगे, या उन्हें सुविधा पर काम करने में अधिक समय लगेगा।

इसी तरह, आपको अपनी गति से काम करना चाहिए और आश्वस्त रहना चाहिए कि आप किसी चीज़ पर काम करने में कितना समय लगा सकते हैं, इसकी कोई कठिन समय सीमा नहीं है। कहा जा रहा है कि, यदि आपको अपने कोड योगदान के किसी भी पहलू से परेशानी हो रही है, तो इस मुद्दे पर मदद मांगने में संकोच न करें, प्रबंधक और अनुरक्षक, साथ ही हमारे समुदाय के सदस्य, आपका मार्गदर्शन करने की पूरी कोशिश करेंगे!


## डेवलपर्स के लिए त्वरित शुरुआत करें

यदि आप एक डेवलपर के रूप में p5.js'🌸 कोडबेस पर काम/योगदान करना चाहते हैं, या तो सीधे p5.js को बेहतर बनाने के लिए या इसके उप-प्रोजेक्ट्स जैसे [फ्रेंडली एरर सिस्टम्स](https://github.com/processing/p5) को बेहतर बनाने के लिए .js/blob/main/contributor_docs/friendly_error_system.md), आप निम्न चरणों का पालन कर सकते हैं:

1. [p5.js का एक कांटा बनाएं](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
2. [अपने बनाए गए फोर्क को अपने कंप्यूटर पर क्लोन करें।](https://docs.github.com/en/repositories/creating-and-maneasing-repositories/cloning-a-repository)
3. [निम्न कमांड का उपयोग करके अपस्ट्रीम जोड़ें](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/configuring-a-remote-repository-ffor-a-fork):

  ```
  git remote add upstream https://github.com/processing/p5.js
  ```

4. सुनिश्चित करें कि आपकी मशीन में [NodeJs](https://nodejs.org/en/download) स्थापित है; इसे निम्न आदेश से जांचें:

  ```
  node -v
  ```

5. इसके साथ निर्भरता स्थापित करें:

  ```
  npm ci
  ```

6. 'मुख्य' शाखा की एक गिट शाखा बनाएं जिसमें वर्णनात्मक शाखा नाम का उपयोग किया जाए:

  ```
  git checkout -b [branch_name]
  ```

7. जैसे ही आप कोडबेस में बदलाव करना शुरू करते हैं, बार-बार परीक्षण चलाएं (इसमें समय लगता है, लेकिन यह सुनिश्चित करता है कि मौजूदा व्यवहार को तोड़ा नहीं जा रहा है)।

  ```
  npm test
  ```

8. यदि आप नई सुविधाएँ जोड़ने या सुविधा बढ़ाने पर काम कर रहे हैं तो कोई भी इकाई परीक्षण जोड़ें।

9. एक बार हो जाने के बाद, आप परिवर्तन कर सकते हैं और एक [पुल अनुरोध](https://p5js.org/contributor-docs/#/./contributor_guidelines?id=pull-requests) बना सकते हैं।


## GitHub संपादन कार्यक्षमता का उपयोग करना

GitHub वेब इंटरफ़ेस पर किसी फ़ाइल को देखते समय, आप जिस फ़ाइल को देख रहे हैं उसकी सामग्री के शीर्ष के पास एक पेंसिल आइकन बटन होगा। यह बटन GitHub द्वारा प्रदान की गई एक सुविधाजनक संपादन सुविधा है जो उन कई प्रक्रियाओं को सरल बनाती है जिन्हें हम नीचे कवर करेंगे और इसका उपयोग आपके द्वारा देखी जा रही फ़ाइल में त्वरित और सरल संपादन करने के लिए किया जा सकता है।

![P5.js रिपॉजिटरी के GitHub में फ़ाइल दृश्य का क्रॉप्ड स्क्रीनशॉट, "src/color/color\_conversion.js" फ़ाइल। एक लाल तीर छवि के दाईं ओर एक पेंसिल आइकन बटन की ओर इशारा करता है।](../images/edit-file.png)

हालाँकि, बहुत ही साधारण परिवर्तनों के अलावा इस सुविधा का उपयोग करने की अनुशंसा नहीं की जाती है। इसका एक मुख्य कारण यह है कि स्रोत कोड में अधिक जटिल परिवर्तनों के लिए, इसे पीआर के रूप में दायर करने से पहले स्थानीय रूप से बनाया और परीक्षण किया जाना चाहिए। इस संपादन कार्यक्षमता द्वारा प्रदान किए गए बुनियादी संपादन वातावरण की तुलना में अधिकांश लोगों के लिए स्थानीय विकास परिवेश का उपयोग करना अक्सर अधिक सहज होता है।


## p5.js को फोर्क करना और अपने फोर्क से काम करना

P5.js स्रोत कोड पर काम करने का पहला चरण p5.js रिपॉजिटरी को फोर्क करना है। ओपन सोर्स में फोर्किंग का एक विशिष्ट अर्थ है, लेकिन हमारे उद्देश्य के लिए, इसका मतलब रिपॉजिटरी की एक प्रति बनाना और इसे अपने GitHub खाते में संग्रहीत करना है। रेपो को फोर्क करने के लिए, बस पृष्ठ के शीर्ष के पास "फोर्क" बटन पर क्लिक करें, और GitHub आपके खाते में रेपो की एक प्रति बना देगा।

![भंडार के मुख्य पृष्ठ का स्क्रीनशॉट। एक बटन, जिस पर फोर्क आइकन और "फोर्क 59.3k" लेबल है, गहरे नारंगी रंग में रेखांकित है।](फोर्क.पीएनजी)

p5.js रिपॉजिटरी के अपने फोर्क से काम करना आवश्यक है क्योंकि आपके पास आधिकारिक p5.js रिपॉजिटरी तक सीधे लिखने की पहुंच नहीं होगी, और फोर्क पर काम करने से आप बदलाव कर सकते हैं और बाद में उन्हें आधिकारिक रिपॉजिटरी में वापस सबमिट कर सकते हैं।


### GitHub डेस्कटॉप का उपयोग करना

GitHub डेस्कटॉप एक प्रोग्राम है जो आपको टर्मिनल में कमांड टाइप करने के बजाय ग्राफिकल यूजर इंटरफेस के माध्यम से git के साथ काम करने देता है। यदि आप git में नए हैं तो यह एक अच्छा विकल्प है, और जब भी आपका मन करे आप Github डेस्कटॉप और टर्मिनल के बीच आगे और पीछे स्विच कर सकते हैं।

सबसे पहले, [GitHub डेस्कटॉप डाउनलोड करें और इंस्टॉल करें।](https://desktop.github.com/) इंस्टॉल होने के बाद, एप्लिकेशन खोलें। यह आपसे आपके GitHub खाते में साइन इन करने के लिए कहेगा। आपके साइन इन करने के बाद, यह आपकी परियोजनाओं को सूचीबद्ध करेगा, जिसमें आपका p5.js का कांटा भी शामिल होगा। अपना कांटा चुनें, जिसका नाम `yourUsername/p5.js` होगा, और नीले "क्लोन" बटन पर क्लिक करें। यह आपके प्रोजेक्ट को कहां रखा जाए, इसके बारे में कुछ विवरण मांगेगा; आप या तो उन्हें बदल सकते हैं या डिफ़ॉल्ट सेटिंग्स छोड़ कर जारी रख सकते हैं।

![साइन इन करने के बाद GitHub डेस्कटॉप उपयोगकर्ता इंटरफ़ेस। स्क्रीन के दाहिने आधे भाग पर, यह आपके प्रोजेक्ट्स को सूचीबद्ध करता है, और नीचे दाईं ओर एक क्लोन बटन।](../images/github-desktop-init.png)

एक बार क्लोन हो जाने पर, यह पूछेगा कि आप अपने फोर्क का उपयोग कैसे करने की योजना बना रहे हैं। मूल प्रोजेक्ट में योगदान करने का विकल्प चुनें और "जारी रखें" पर क्लिक करें।

![कांटा क्लोन करने के बाद का दृश्य। यह पूछता है कि क्या आप मूल परियोजना में योगदान करने की योजना बना रहे हैं, या इसे अपने उद्देश्यों के लिए उपयोग करने की योजना बना रहे हैं।](../images/github-desktop-fork.png)


### `गिट` कमांड लाइन इंटरफ़ेस का उपयोग करना

एक बार फोर्क बन जाने के बाद, अपने फोर्क के पेज पर जाएं और हरे "कोड" बटन पर क्लिक करके गिट यूआरएल को कॉपी करें। इसे कुछ इस तरह दिखना चाहिए `https://github.com/limzykenneth/p5.js.git`.

![रिपॉजिटरी के लैंडिंग पृष्ठ पर फ़ाइलों की सूची का स्क्रीनशॉट। "कोड" बटन को गहरे नारंगी रंग की रूपरेखा से हाइलाइट किया गया है।](../images/code-button.png)

इसके बाद अपने स्थानीय वातावरण में कमांड लाइन पर जाएं और इस गिट रिपॉजिटरी को क्लोन करें। "क्लोन" का सीधा सा अर्थ है अपने स्थानीय मशीन पर रेपो की एक प्रति डाउनलोड करना। उस फ़ोल्डर में निम्न आदेश चलाएँ जहाँ आप p5.js स्रोत कोड फ़ोल्डर संग्रहीत करना चाहते हैं।

```
गिट क्लोन [git_url]
```

`[git_url]` को उस यूआरएल से बदलें जिसे आपने अभी ऊपर कॉपी किया है। आपके इंटरनेट कनेक्शन की गति के आधार पर इसमें कई मिनट लग सकते हैं, कुछ कॉफ़ी बनाने का यह एक अच्छा समय है! एक बार प्रक्रिया समाप्त हो जाने पर, आप अपने पसंदीदा टेक्स्ट एडिटर में `p5.js` नामक डाउनलोड किए गए फ़ोल्डर को खोल सकते हैं और चारों ओर देखना शुरू कर सकते हैं।


## कोडबेस ब्रेकडाउन

आपके पास p5.js फ़ोल्डर में मौजूद कुछ प्रमुख फ़ाइलें और फ़ोल्डर इस प्रकार हैं:

- `src` - जहां सभी कोड जो अंततः अंतिम p5.js और p5.min.js फ़ाइलों में संयुक्त हो जाते हैं, रहते हैं
- [`test`](https://github.com/processing/p5.js/blob/main/contributor_docs/unit_testing.md) - जहां सभी दस्तावेज़ उदाहरणों के परीक्षण के लिए इकाई परीक्षण और कोड रहता है
- `कार्य` - जहां विस्तृत और कस्टम बिल्ड कोड रहता है
- `Gruntfile.js` - यह मुख्य बिल्ड कॉन्फ़िगरेशन फ़ाइल है
- `contributor_docs` - जहां दस्तावेज़ और अन्य सभी योगदानकर्ता दस्तावेज़ रहते हैं

अन्य फ़ाइलें और फ़ोल्डर्स या तो कॉन्फ़िगरेशन हैं या अन्य प्रकार की समर्थन फ़ाइलें हैं; अधिकांश मामलों में, आपको कोई संशोधन करने की आवश्यकता नहीं होनी चाहिए।


## सेटअप बनाएं

कुछ भी करने से पहले, आपको स्थानीय प्रोजेक्ट फ़ोल्डर सेट करना होगा ताकि आप p5.js के लिए परीक्षण बना और चला सकें। यह मानते हुए कि आपके पास नोड.जेएस स्थापित है, चलाएँ:

```
npm ci
```

इसमें कुछ समय लगने की संभावना है, क्योंकि एनपीएम सभी आवश्यक निर्भरताएँ डाउनलोड करता है। हालाँकि, एक बार हो जाने के बाद, बस, आप पूरी तरह तैयार हैं। बहुत सरल, है ना?


## गिट वर्कफ़्लो

अब, आप आवश्यक परिवर्तन करने के लिए तैयार हैं; रिपॉजिटरी के विभिन्न हिस्सों के बारे में अधिक जानकारी के लिए और आप प्रासंगिक परिवर्तन कैसे कर सकते हैं, नीचे दिए गए उपखंड देखें। आरंभ करने के लिए, चलाएँ:

```
npm test
```

शुरुआत से p5.js बनाने का प्रयास करने और सभी यूनिट परीक्षण चलाने के लिए, इसे बिना किसी त्रुटि के पूरा करना चाहिए। यदि आप परीक्षण चलाए बिना केवल लाइब्रेरी बनाना चाहते हैं, तो आप चला सकते हैं:

```
npm run build
```

उपरोक्त में से कोई भी आदेश लाइब्रेरी को `lib/` फ़ोल्डर में `p5.js` और `p5.min.js` के रूप में बनाएगा। यदि आवश्यक हो तो आप इन निर्मित फ़ाइलों का उपयोग अपने परीक्षणों के लिए कर सकते हैं।

इसके बाद, हम अनुशंसा करते हैं कि आप अपना काम शुरू करने से पहले `मुख्य' शाखा से एक शाखा बना लें। जैसा कि नाम से पता चलता है, गिट में एक शाखा रेपो का एक शाखित संस्करण है जिसे आप 'मुख्य' या अन्य शाखाओं को प्रभावित किए बिना कमिट जोड़ सकते हैं। शाखाएँ आपको एक साथ कई सुविधाओं पर काम करने में सक्षम बनाती हैं (कई अलग-अलग शाखाओं का उपयोग करके) और आपको विश्वास है कि यदि आप किसी शाखा में गड़बड़ी करते हैं तो यह 'मुख्य' शाखा को प्रभावित नहीं करेगी।

GitHub डेस्कटॉप में, यह विंडो के हेडर में करंट ब्रांच बटन पर क्लिक करके किया जा सकता है। यहां से, आप शाखाएं बदल सकते हैं, या नई शाखा बनाने के लिए शाखा का नाम दर्ज कर सकते हैं। हमारे उद्देश्यों के लिए, आपके द्वारा किए जाने वाले परिवर्तन का वर्णन करते हुए एक नई शाखा का नाम दर्ज करें और नई शाखा बनाएं पर क्लिक करें।

![GitHub डेस्कटॉप शाखा चयन मेनू का एक स्क्रीनशॉट। एक नई शाखा का नाम दर्ज करने के बाद जो अभी तक मौजूद नहीं है, एक "नई शाखा बनाएं" बटन दिखाई देता है।](../images/github-desktop-create-branch.png)

टर्मिनल से, जब आप `मुख्य` शाखा पर हों तो `git checkout -b ब्रांच_नाम` चलाएँ, `branch_name` को किसी वर्णनात्मक चीज़ से बदलें, और अब आप एक अलग शाखा पर होंगे।

जैसे ही आप अपने परिवर्तन करते हैं, हम `npm test` को बार-बार चलाने की सलाह देते हैं, खासकर यदि आप स्रोत कोड पर काम कर रहे हैं। इसे चलाने में कुछ समय लगेगा, लेकिन यह सुनिश्चित करता है कि आपके द्वारा किए गए परिवर्तन मौजूदा व्यवहार को नहीं तोड़ रहे हैं। नीचे बताए अनुसार परिवर्तन करने से पहले आपको `npm test` चलाना चाहिए।

एक बार जब आप कोडबेस में अपने परिवर्तन कर लेते हैं, तो आपको इसे गिट में प्रतिबद्ध करना होगा। कमिट गिट रिपॉजिटरी में सहेजे गए परिवर्तनों का एक संग्रह है; यह अनिवार्य रूप से प्रतिबद्धता के समय रेपो में फ़ाइलों की वर्तमान स्थिति को रिकॉर्ड करता है।

एक प्रश्न उठ सकता है कि आपको कितनी बार गिट के लिए प्रतिबद्ध होना चाहिए? सामान्य तौर पर यह प्राथमिकता दी जाती है कि आप कई बड़े बदलावों को एक प्रतिबद्धता में डालने के बजाय बार-बार प्रतिबद्ध होने का लक्ष्य रखें। एक अच्छा दिशानिर्देश यह है कि जब भी आप कोई ऐसा उपकार्य पूरा कर लें जिसे एक वाक्य में वर्णित किया जा सके तो उसे प्रतिबद्ध कर दें।

GitHub डेस्कटॉप से ​​सभी मौजूदा परिवर्तन करने के लिए, अपने परिवर्तन करने के बाद ऐप खोलें। यह बाएं साइडबार में आपके द्वारा बदली गई फ़ाइलों की एक सूची दिखाएगा, और दाईं ओर प्रत्येक फ़ाइल के भीतर विशिष्ट परिवर्तन दिखाएगा। विंडो के निचले बाएँ कोने में अपने उपयोगकर्ता आइकन के बगल वाले फ़ील्ड में एक संक्षिप्त, उच्च-स्तरीय विवरण टाइप करें। यह कमिट का शीर्षक होगा. आप नीचे विवरण फ़ील्ड में और विस्तार से बता सकते हैं या इसे खाली छोड़ सकते हैं। परिवर्तन को अंतिम रूप देने के लिए नीले "प्रतिबद्ध" बटन पर क्लिक करें।

![परिवर्तन करने के बाद GitHub डेस्कटॉप का एक स्क्रीनशॉट। वह क्षेत्र जहां आपको अपने परिवर्तन के लिए शीर्षक लिखना है, विंडो के नीचे बाईं ओर लाल रंग में दर्शाया गया है।](../images/github-desktop-commit.png)

टर्मिनल से सभी मौजूदा परिवर्तन करने के लिए, निम्नलिखित चलाएँ:

1. जांचें कि यह केवल उन फ़ाइलों को सूचीबद्ध करता है जिन्हें आपने निम्न आदेश के साथ बदला है।

```
git status
```

यदि सूचीबद्ध फ़ाइलें हैं जिन्हें आपने नहीं बदला है, तो आपको या तो उन्हें मूल रूप में [पुनर्स्थापित](https://git-scm.com/docs/git-restore) करना होगा या सुनिश्चित करना होगा कि वे इच्छित परिवर्तन हैं। प्रत्येक फ़ाइल के लिए अधिक विस्तृत परिवर्तन दिखाने के लिए निम्न आदेश का उपयोग करें।

```
git diff
```

आपको कोई भी फ़ाइल परिवर्तन नहीं करना चाहिए जिसे आप अपने पीआर के लिए बदलने का इरादा नहीं रखते हैं।

2. निम्नलिखित आदेश के साथ गिट में प्रतिबद्ध होने के लिए सभी परिवर्तनों को चरणबद्ध करें।

```
git add .
```

3. Git में परिवर्तन करने के लिए, निम्न कमांड चलाएँ।

```
git commit -m "[your_commit_message]"
```

`[your_commit_message]` को एक प्रासंगिक प्रतिबद्ध संदेश के साथ प्रतिस्थापित किया जाना चाहिए जो सामान्य बयानों से बचते हुए परिवर्तनों का वर्णनात्मक हो। उदाहरण के लिए, 'डॉक्यूमेंटेशन फिक्स 1' कहने के बजाय, 'सर्कल() फ़ंक्शन में दस्तावेज़ उदाहरण जोड़ें' कहें।

```
git commit -m "Add documentation example to circle() function"
```

यह सुनिश्चित करने के लिए कि चीजें काम कर रही हैं, समय-समय पर `एनपीएम टेस्ट` चलाना सुनिश्चित करते हुए आपके द्वारा किए जा रहे सभी कमिट के लिए उपरोक्त चरणों को दोहराएं।


### सोर्स कोड

यदि आप स्रोत कोड पर काम करने जा रहे हैं, तो शुरुआत करने के लिए एक अच्छी जगह है, यदि आप जानते हैं कि आप किस p5.js सुविधाओं पर काम करने जा रहे हैं, तो प्रलेखन पर जाएँ और p5.js की प्रत्येक प्रलेखित कार्यक्षमता के नीचे जाएँ। इसके सोर्स कोड का लिंक होगा।

![p5.js वेबसाइट पर एक संदर्भ पृष्ठ का क्रॉप किया गया स्क्रीनशॉट जिसमें वाक्य है "किसी भी त्रुटि या टाइपो पर ध्यान दें? कृपया हमें बताएं। कृपया बेझिझक src/core/shape/2d\_primitives.js को संपादित करें और एक पुल अनुरोध जारी करें !". उपरोक्त वाक्य का वह भाग जहां यह कहता है "src/core/shape/2d\_primitives.js" को लाल रेखा और तीर की ओर इंगित करते हुए हाइलाइट किया गया है।](../images/reference-code-link.png)


### यूनिट परीक्षण

यदि आप यूनिट परीक्षणों पर काम करने जा रहे हैं, तो कृपया [यहां] (https://github.com/processing/p5.js/blob/main/contributor_docs/unit_testing.md) देखें। ध्यान दें कि किसी भी सुविधा वृद्धि, नई सुविधाओं और कुछ बग फिक्स के लिए, नए कार्यान्वयन को कवर करने वाले यूनिट परीक्षणों को पीआर में शामिल किया जाना चाहिए।


### इनलाइन दस्तावेज़ीकरण

यदि आप इनलाइन दस्तावेज़ीकरण पर काम करने जा रहे हैं, तो कृपया [यहां](https://github.com/processing/p5.js/blob/main/contributor_docs/inline_documentation.md) देखें।


### अभिगम्यता

यदि आप एक्सेसिबिलिटी सुविधाओं पर काम करने जा रहे हैं, तो कृपया [यहां] (https://github.com/processing/p5.js/blob/main/contributor_docs/web_accessibility.md) देखें। एक अनुकूल त्रुटि प्रणाली के लिए, कृपया [यहां](https://github.com/processing/p5.js/blob/main/contributor_docs/friendly_error_system.md) देखें।


## कोड मानक

p5.js का कोड मानक या कोड शैली [ESLlint](https://eslint.org/) द्वारा लागू की जाती है। किसी भी गिट कमिट और पुल अनुरोध को स्वीकार करने से पहले उसे लिंटिंग से गुजरना होगा। आपके लिए सही कोडिंग मानक का पालन करने का सबसे आसान तरीका आपके टेक्स्ट एडिटर के लिए लिंटिंग एरर हाइलाइटिंग (अधिकांश लोकप्रिय टेक्स्ट संपादकों के लिए उपलब्ध) के साथ उपलब्ध ESLint प्लगइन का उपयोग करना है।


## सॉफ़्टवेयर डिज़ाइन सिद्धांत

P5.js की किसी भी सुविधा पर काम करते समय, p5.js के डिज़ाइन सिद्धांतों को ध्यान में रखना महत्वपूर्ण है। हमारी प्राथमिकताएँ अन्य परियोजनाओं की प्राथमिकताओं से भिन्न हो सकती हैं, इसलिए यदि आप किसी भिन्न परियोजना से आ रहे हैं, तो हम अनुशंसा करते हैं कि आप स्वयं को p5.js के डिज़ाइन सिद्धांतों से परिचित करा लें।

- **पहुंच** हम सबसे पहले पहुंच को प्राथमिकता देते हैं, और हमारे द्वारा लिए गए निर्णयों में इस बात को ध्यान में रखना चाहिए कि यह ऐतिहासिक रूप से हाशिए पर रहने वाले समूहों तक पहुंच कैसे बढ़ाता है। हमारे एक्सेस स्टेटमेंट में इसके बारे में और पढ़ें।
- **शुरुआती अनुकूल** p5.js एपीआई का लक्ष्य शुरुआती कोडर्स के लिए अनुकूल होना है, जो अत्याधुनिक HTML5/कैनवस/DOM एपीआई के साथ इंटरैक्टिव और विज़ुअल वेब सामग्री बनाने में कम बाधा प्रदान करता है।
- **शैक्षिक** p5.js एक एपीआई और पाठ्यक्रम पर केंद्रित है जो शैक्षिक उपयोग का समर्थन करता है, जिसमें सहायक उदाहरणों के साथ एपीआई का पूरा संदर्भ, साथ ही ट्यूटोरियल और नमूना कक्षा पाठ्यक्रम शामिल हैं जो मुख्य रचनात्मक कोडिंग सिद्धांतों को स्पष्ट रूप से पेश करते हैं। आकर्षक आदेश.
- **जावास्क्रिप्ट और उसका समुदाय** p5.js का उद्देश्य उचित जावास्क्रिप्ट डिज़ाइन पैटर्न और उपयोग को मॉडलिंग करके शुरुआती लोगों के लिए वेब विकास प्रथाओं को अधिक सुलभ बनाना है, जबकि आवश्यक होने पर उनका सार तैयार करना है। एक ओपन-सोर्स लाइब्रेरी के रूप में, p5.js में इसके निर्माण, दस्तावेज़ीकरण और प्रसार में व्यापक जावास्क्रिप्ट समुदाय भी शामिल है।
- **प्रसंस्करण और उसका समुदाय** p5.js प्रसंस्करण भाषा और उसके समुदाय से प्रेरित है और इसका उद्देश्य प्रसंस्करण जावा से जावास्क्रिप्ट में परिवर्तन को आसान और स्पष्ट बनाना है।

[**⬆ शीर्ष पर वापस**](#योगदानकर्ता-दिशानिर्देश)

---


# Pull requests

Now that you have made the changes you need to make, including unit tests if applicable, `npm test` does not error, and you have committed the changes, you can start preparing pull requests to get your new commits merged into the official p5.js repository. A pull request, more formally, is a request to a repo (in this case, the official p5.js repo) to pull or merge changes from another repo (in this case, your forked p5.js repo) into its commit history.


## Creating a pull request

The first step here is to push your new commits to your fork of p5.js; think of it as uploading the changes to your fork.

From GitHub Desktop, just to the right of the button to change branches in the header is a button to push your changes to GitHub. Click this to push your changes.![A view of GitHub Desktop after committing changes. The button to push the changes online is circled in red.](../images/publish-branch.png)

Once your code is uploaded, it will show a button prompting you to create a pull request. Clicking the button once will show a preview with another button to actually create the request. Press the "Create Pull Request" button to begin the process.

![A screenshot of Github Desktop after pushing code. In the left sidebar, it says "0 changed items." In the right pane, below the "No local changes" header, a blue "Review Pull Request" button has been marked up with a red circle.](../images/preview-pull-request.png)

From the terminal, run the following command:

```
git push -u origin [branch_name]
```

Once the push is complete, you may see a link in the terminal that lets you open a pull request, if not you can navigate to your fork in your web browser, switch to the branch you are working on with the dropdown button on top of the file list, click on "Contribute" then "Open pull request."

![](https://lh7-us.googleusercontent.com/xoqM9gLSFXyw7b3gzG8JlHqoO0zxHALbjSz93E3D0HNh4Jw2wDWdzHKUEchnB6hdjQC7hVn-o5prrXkLw2WiEOoVKJF6kpmyA65sirN0z-Vy3PBY3rCXC5Ifn5stQhcdUQxQS0rsVoW0_hlkfTcY8PQ)

You may also see a button to open a pull request when you visit the p5.js Github repo. Clicking it will also work to open a new pull request.

![Cropped screenshot of the main page of the p5.js GitHub repository web page. A section near the top of the page is a yellow call to action box containing a green button with the text "Compare & pull request".](../images/recent-pushes)


### Pull request information

![Screenshot of an "Open a pull request" page on GitHub that is prepopulated with p5.js's pull request template.](../images/new-pr.png)

Before filing the pull request, you will need to fill out the pull request template. 


### Title

The pull request title should briefly describe what the changes are, again avoid generic statements here.


### Resolves

In the template, there is this line `Resolves #[Add issue number here]`, which you should replace `[Add issue number here]` with the issue number of the issue you are addressing/fixing [above](https://github.com/processing/p5.js/blob/main/contributor_docs/contributor_guidelines.md#all-about-issues) (e.g., `Resolves #1234`). This will make sure the issue is automatically closed after this PR is merged. If you do not wish to automatically close the issue after this PR is merged (maybe because there are more changes coming in a separate PR), change `Resolves` to `Addresses`.


### Changes

You should clearly describe the changes you have made in this PR. Include any implementation details and decisions you made here that are relevant to whoever will review it.


### Screenshots of the change

This is optional depending on circumstances and should be included when making changes related to how p5.js renders visuals on the canvas. Note that this is not a screenshot of the text editor but a screenshot of an example sketch's behavior after your changes.


### PR Checklist

This contains some relevant checklist items that you should tick by replacing `[ ]` with `[x]` wherever relevant to your changes.

Once done, click on "Create pull request."


### Rebase and resolve conflicts

![Screenshot of an open pull request on p5.js's GitHub repository. The title of the pull request says "Fix filter shaders when rectMode is applied; add tests #6603.](../images/opened-pr.png)

You should now inspect the opened pull request and pay attention to a few things:

1. The number of commits should match the number of commits you have made, meaning if you have committed two times while working on this PR, it should only show two commits in the "Commits" tab.
2. The "Files changed" tab should show the changes you have made as compared to the p5.js repo and nothing more.
3. Near the bottom, it should say, "This branch has no conflicts with the base branch," and not "This branch has conflicts that must be resolved."

If any of the above is not true (there are more commits than you expected or there are conflicts), you may need to [rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) or help resolve conflicts. Conflicts here mean that you have made changes to a file that also recently had changes applied to it, and git is not sure which set of changes to keep or leave out. If you are not confident in resolving these issues, let us know and we'll guide you through the process. Basic instruction is as below.

Sometimes, Github lets you resolve conflicts directly in the browser by showing you a Resolve Conflicts button:![A screenshot of a GitHub pull request with merge conflicts. The conflicting filenames are listed, and there is a "Resolve conflicts" button highlighted.](../images/resolve-conflicts.png)

Conflicts are shown between `<<<<<<<` and `>>>>>>>`, separated by `=======`. One section shows your code, and the other section shows what has changed in the main branch.

![A screenshot of GitHub's conflict resolution interface. A sidebar lists the files with conflicts. The right pane contains the conflicting code, with merge conflict markers highlighted.](../images/conflicts-interface.png)

Remove the conflict markers and keep just the final code that you want in your PR. You can click "Mark as resolved" when all the conflicts have been addressed.

![A screenshot of the GitHub conflict resolution interface after editing the code to remove the merge conflict markers. The "mark as resolved" button in the upper right is enabled.](../images/mark-as-resolved.png)

When all files with conflicts have been resolved, you can commit your changes.

![The GitHub conflict resolution interface after all conflicts have been marked as resolved. A green "commit merge" button is enabled.](../images/commit-merge.png)

Sometimes, the conflicts are too complicated for Github to show on the web. In this case, or if you just prefer the manual method, you can resolve your conflicts locally:

1. Run `git remote add upstream https://github.com/processing/p5.js`
2. Run `git fetch upstream`
3. Run `git rebase upstream/main`
4. You may have some conflicts! If it’s just lib/p5.js and lib/p5.min.js, it’s easy to fix; just build the project again. If you have conflicts in other files & you're not sure how to resolve them, ask for help!

```
npm test
git add -u
git rebase --continue
```

5. Run `git push`

The checklist above may clear out after these steps but if not, we'll guide you through any fix necessary.


## Discuss and amend

Now that your PR is opened, a steward or maintainer will review your PR. It may take several days before a steward is able to reply to your PR, so be patient. Why not use the time to check out some of the other open issues in the meantime?

Once a steward has reviewed your PR, one of two things may happen: 1. Your PR is approved and merged, hurray! 2. The steward may ask some questions regarding the PR or request some changes to the PR. If it's the latter, don't panic; it's perfectly normal, and the stewards are always here to help you complete your contribution!

If changes are requested of your PR and you are able to make those changes, follow the [same process as before](https://github.com/processing/p5.js/blob/main/contributor_docs/contributor_guidelines.md#git-workflow) but just continue from your local copy of the repo and relevant branch, make those changes, commit them into git, and push them to your forked remote repo. Once you have pushed additional commits to your forked remote repo, you will see that the new commits automatically show up in the PR. Leave a comment in the PR to let the reviewer know you have made the requested changes, and if no additional changes are needed, your PR will be merged!

[**⬆ back to top**](#contributor-guidelines)

