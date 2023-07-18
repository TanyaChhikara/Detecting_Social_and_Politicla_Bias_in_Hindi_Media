<h1>Detecting Social and Political Bias in Hindi News Media</h1>

<h3>About The Project</h3>
<p> Media in different forms, print or electronic, has been a source of information for hundreds of years. From providing general knowledge
to shaping public opinion, the media has always significantly impacted
readers. Media is presumed to be truthful, fair, and accurate. However,
prior works have shown biased reporting mostly by popular English news
media. In this work, we have focused on Indian (Hindi) media and highlighted political and social bias using our Natural Language Processing
models. We collected the data from three different Hindi media websites
(NDTV, The Quint, and ZEE News) and focused on four major events
(political and social). More than 10000 articles were extracted and annotated into three categories each for political and social. Obtained data
was pre-processed and multiple baseline machine learning models such as
Logistic Regression, Naive Bayes, Decision Trees, SVM, Random Forest,
and RNN were implemented. The best performance was given by logistic
regression with an accuracy of 64.% for political news and 58% for social news for three class prediction. Moreover, we observed that the title
and text in news articles were the best indicators for detecting biases. </p>

<h3>Dataset Description and Annotation</h3>
We extracted the news articles from different Hindi media websites namely NDTV, Zee News, and The Quint Hindi. The reason to select these news websites is to get diverse news articles. Zee News is known for its pro-BJP stories and for being supporters of right-wing, whilst NDTV and The Quint are known for being more liberal media outlets and more critical of the present BJP-led Government. Major events that we have chosen for the research are Kisan Andolan, Hijab Controversy, Money Laundering and Communal Riots. We collected news articles related to each of these events. For each news article, we collected news title, news description, source name from where it is extracted and the date of publishing of the news article. In total, we collected 11000 articles from the 4 news sources. We manually inspected and eliminated any irrelevant articles. Finally, a total of 1169 news articles remained, of which 550 were related to Kisan Andolan, 272 were related to Hijab Controversy, 221 were related to Money Laundering and the rest 126 were related to Communal Riots (Nupur Sharma’s Controversy). Figure 2 depicts the event-wise distribution of the number of articles collected from different news sources. The pie charts in Figure 3 are a representation of the number of articles on the 4 events that were taken from the news sources. The dataset below depicts the social and political bias of news articles with the categories of Pro Hindu, Pro Muslim, or neutral for social bias and Pro Bhartiya Janata Party2, Anti Bhartiya Janata Party or neutral for political bias. To summarize the textual data, event wise word clouds have been made along with bar chart representing the distribution of total number of articles and the 4 news events. 
news events.
<br>
<h3> Example Dataset</h3>
<google-sheets-html-origin style="color: rgb(0, 0, 0);"><table xmlns="http://www.w3.org/1999/xhtml" cellspacing="0" cellpadding="0" dir="ltr" border="1" style="table-layout: fixed; font-size: 10pt; font-family: Arial; width: 0px; border-collapse: collapse; border: none;">
  <thead>
    <tr style="height: 21px;">
      <th>news_title</th>
      <th>Social Bias</th>
    </tr>
  </thead><colgroup><col width="657"><col width="281"></colgroup>
  <tbody>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;जो कुरान पढ़ते हैं...' : हिंदू संगठन के नेता के खिलाफ हेट स्पीच का मामला दर्ज&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">जो कुरान पढ़ते हैं...' : हिंदू संगठन के नेता के खिलाफ हेट स्पीच का मामला दर्ज</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;इस सवाल पर कि आरिफ मोहम्‍मद खान ने कहा है कि जो कट्टरवाद पैदा हो रहा उसके पीछे मुख्‍य रूप से मदरसे है जो गलत शिक्षा दे रहे हैं, जंग ने कहा, \&quot;आरिफ साब विद्वान हैं. मैं उनकी बेहद इज्‍जत करता हूं लेकिन उनकी इस बात से इत्‍तेफाक नहीं रखता. देश के स्‍वाधीनता आंदोलन में मदरसों का अहम योगदान रहा है. \&quot;&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">इस सवाल पर कि आरिफ मोहम्‍मद खान ने कहा है कि जो कट्टरवाद पैदा हो रहा उसके पीछे मुख्‍य रूप से मदरसे है जो गलत शिक्षा दे रहे हैं, जंग ने कहा, "आरिफ साब विद्वान हैं. मैं उनकी बेहद इज्‍जत करता हूं लेकिन उनकी इस बात से इत्‍तेफाक नहीं रखता. देश के स्‍वाधीनता आंदोलन में मदरसों का अहम योगदान रहा है. "</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;मुस्लिमों को लेकर संगीतकार विशाल ददलानी का ट्वीट- 'आपका दर्द हमारा दर्द', शशि थरूर ने कहा- \&quot;शाबाश...\&quot;&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">मुस्लिमों को लेकर संगीतकार विशाल ददलानी का ट्वीट- 'आपका दर्द हमारा दर्द', शशि थरूर ने कहा- "शाबाश..."</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;‘पैगंबर के अपमान’ को लेकर नागपुर के विज्ञान संस्थान की वेबसाइट हैक, हैकर ने अपनी पहचान भी बताई&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">‘पैगंबर के अपमान’ को लेकर नागपुर के विज्ञान संस्थान की वेबसाइट हैक, हैकर ने अपनी पहचान भी बताई</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Deshhit: पैगंबर का अपमान...'सिर कलम' का फरमान&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Deshhit: पैगंबर का अपमान...'सिर कलम' का फरमान</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;कौन हैं विवादों के 'राजा'? किया पैगंबर का अपमान, पहले 6 बार कर चुके हैं ये 'काम'&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">कौन हैं विवादों के 'राजा'? किया पैगंबर का अपमान, पहले 6 बार कर चुके हैं ये 'काम'</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Madhya Pradesh: पिता को आया मैसेज -- आपका बेटा बहादुर था, लेकिन 'गुस्ताख ए रसूल की एक ही सजा'&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Madhya Pradesh: पिता को आया मैसेज -- आपका बेटा बहादुर था, लेकिन 'गुस्ताख ए रसूल की एक ही सजा'</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;कन्हैया लाल और नूपुर शर्मा का समर्थन पड़ा भारी, अब वकील को सिर कलम करने की धमकी&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">कन्हैया लाल और नूपुर शर्मा का समर्थन पड़ा भारी, अब वकील को सिर कलम करने की धमकी</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;एक जुलाई को कुछ हिंदू संगठन के कार्यकर्ता राजस्थान के उदयपुर में दर्जी कन्हैया लाल की हत्या को लेकर विरोध प्रदर्शन कर रहे थे, उस दौरान यह बयान दिया गया.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">एक जुलाई को कुछ हिंदू संगठन के कार्यकर्ता राजस्थान के उदयपुर में दर्जी कन्हैया लाल की हत्या को लेकर विरोध प्रदर्शन कर रहे थे, उस दौरान यह बयान दिया गया.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नूपुर शर्मा ने पिछले महीने एक टीवी डिबेट के दौरान पैगंबर मोहम्मद पर आपत्तिजनक टिप्पणी की थी. जिसपर ईरान, इराक, कुवैत, कतर, सऊदी अरब, ओमान, यूएई, जॉर्डन, अफगानिस्तान, बहरीन, मालदीव, लीबिया और इंडोनेशिया सहित कम से कम 15 देशों ने आधिकारिक विरोध जताया है.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नूपुर शर्मा ने पिछले महीने एक टीवी डिबेट के दौरान पैगंबर मोहम्मद पर आपत्तिजनक टिप्पणी की थी. जिसपर ईरान, इराक, कुवैत, कतर, सऊदी अरब, ओमान, यूएई, जॉर्डन, अफगानिस्तान, बहरीन, मालदीव, लीबिया और इंडोनेशिया सहित कम से कम 15 देशों ने आधिकारिक विरोध जताया है.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;देश के कुछ हिस्सों में भाजपा की निलंबित प्रवक्ता नूपुर शर्मा और पार्टी से निष्कासित नेता नवीन कुमार जिंदल द्वारा पैगंबर मोहम्मद के खिलाफ की गई कथित आपत्तिजनक टिप्पणी के विरोध के बीच इंस्टीट्यूट ऑफ साइंस की वेबसाइट को हैक किए जाने की यह घटना सामने आई है.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">देश के कुछ हिस्सों में भाजपा की निलंबित प्रवक्ता नूपुर शर्मा और पार्टी से निष्कासित नेता नवीन कुमार जिंदल द्वारा पैगंबर मोहम्मद के खिलाफ की गई कथित आपत्तिजनक टिप्पणी के विरोध के बीच इंस्टीट्यूट ऑफ साइंस की वेबसाइट को हैक किए जाने की यह घटना सामने आई है.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;बीजेपी विधायक टी. राजा सिंह की पैगंबर साहब पर आपत्तिजनक टिप्पणी से तेलंगाना में बवाल बढ़ गया. आज उन्हें इस मामले में गिरफ्तार भी किया गया. राजा सिंह के वकील ने दावा किया है कि कोर्ट ने उन्हें फौरन रिहा करने का आदेश दिया है. पैगंबर साहब के अपमान का आरोप लगने के बाद BJP ने राजा सिंह को निलंबित कर दिया है और साथ ही उन्हें शो कॉज नोटिस भी जारी किया गया है.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">बीजेपी विधायक टी. राजा सिंह की पैगंबर साहब पर आपत्तिजनक टिप्पणी से तेलंगाना में बवाल बढ़ गया. आज उन्हें इस मामले में गिरफ्तार भी किया गया. राजा सिंह के वकील ने दावा किया है कि कोर्ट ने उन्हें फौरन रिहा करने का आदेश दिया है. पैगंबर साहब के अपमान का आरोप लगने के बाद BJP ने राजा सिंह को निलंबित कर दिया है और साथ ही उन्हें शो कॉज नोटिस भी जारी किया गया है.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;BJP से निलंबित किए गए विधायक टी राजा आखिर कौन हैं? जो अपनी विवादित टिप्पणी के चलते एक बार फिर सुर्खियों में हैं. ऐसा नहीं है कि उन्होंने पहली बार कोई आपत्तिजनक बयानबाजी की हो, इससे पहले भी कई बार वो ऐसा कर चुके हैं. इस बार उन्हें पार्टी से निलंबित कर दिया गया.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">BJP से निलंबित किए गए विधायक टी राजा आखिर कौन हैं? जो अपनी विवादित टिप्पणी के चलते एक बार फिर सुर्खियों में हैं. ऐसा नहीं है कि उन्होंने पहली बार कोई आपत्तिजनक बयानबाजी की हो, इससे पहले भी कई बार वो ऐसा कर चुके हैं. इस बार उन्हें पार्टी से निलंबित कर दिया गया.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;मध्य प्रदेश के रायसेन जिले में इंजीनियरिंग स्टूडेंट की हुई हत्या के मामले में पिता को Whatsapp पर जो संदेश मिला वो हैरान करने वाला था. मैसेज में मौत को लेकर 'सर तन से जुदा' का जिक्र किया गया था.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">मध्य प्रदेश के रायसेन जिले में इंजीनियरिंग स्टूडेंट की हुई हत्या के मामले में पिता को Whatsapp पर जो संदेश मिला वो हैरान करने वाला था. मैसेज में मौत को लेकर 'सर तन से जुदा' का जिक्र किया गया था.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;गाजियाबाद के वकील के घर पर 'सिर तन से जुदा' के पोस्टर चस्पा होने का मामला सामने आया है. बताया जा रहा है कि थाना ट्रॉनिका सिटी इलाके में आवास विकास कॉलोनी में रहने वाले वकील को असामाजिक तत्वों सिर तन से अलग करने की धमकी दी है.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">गाजियाबाद के वकील के घर पर 'सिर तन से जुदा' के पोस्टर चस्पा होने का मामला सामने आया है. बताया जा रहा है कि थाना ट्रॉनिका सिटी इलाके में आवास विकास कॉलोनी में रहने वाले वकील को असामाजिक तत्वों सिर तन से अलग करने की धमकी दी है.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Muslim&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Muslim</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;अमरावती (Amravati) में मेडिकल स्टोर के मालिक उमेश कोल्हे की हत्या (Umesh Kolhe murder) सिर्फ इसलिए कर दी गई थी, क्योंकि उन्होंने नुपुर शर्मा(Nupur Sharma) के समर्थन में सोशल मीडिया पर पोस्ट लिखा था. जांच एजेंसी एनआईए इस मामले में अभी तक आठ के करीब आरोपियों को गिरफ्तार कर चुकी है.&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">अमरावती (Amravati) में मेडिकल स्टोर के मालिक उमेश कोल्हे की हत्या (Umesh Kolhe murder) सिर्फ इसलिए कर दी गई थी, क्योंकि उन्होंने नुपुर शर्मा(Nupur Sharma) के समर्थन में सोशल मीडिया पर पोस्ट लिखा था. जांच एजेंसी एनआईए इस मामले में अभी तक आठ के करीब आरोपियों को गिरफ्तार कर चुकी है.</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नूपुर शर्मा के समर्थन में पोस्ट करने पर अहमदनगर में युवक पर जानलेवा हमला&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नूपुर शर्मा के समर्थन में पोस्ट करने पर अहमदनगर में युवक पर जानलेवा हमला</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नूपुर शर्मा की हत्या की साज़िश के पीछे पाकिस्तानी संगठन, सीमापार से भेजा आतंकी गिरफ्तार&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नूपुर शर्मा की हत्या की साज़िश के पीछे पाकिस्तानी संगठन, सीमापार से भेजा आतंकी गिरफ्तार</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;MP: नूपुर शर्मा का समर्थन करने पर बजरंग दल के कार्यकर्ता पर हमला, दो गिरफ्तार&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">MP: नूपुर शर्मा का समर्थन करने पर बजरंग दल के कार्यकर्ता पर हमला, दो गिरफ्तार</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नूपुर शर्मा की हत्या के इरादे से भारतीय सीमा में घुसा पाकिस्तानी युवक गिरफ्तार&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नूपुर शर्मा की हत्या के इरादे से भारतीय सीमा में घुसा पाकिस्तानी युवक गिरफ्तार</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;\&quot;उनकी जिंदगी, आजादी की रक्षा करने की जरूरत है\&quot;: नूपुर शर्मा को राहत देते हुए सुप्रीम कोर्ट&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">"उनकी जिंदगी, आजादी की रक्षा करने की जरूरत है": नूपुर शर्मा को राहत देते हुए सुप्रीम कोर्ट</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;इंस्टाग्राम पर नुपुर शर्मा की तस्वीर डालने पर कारोबारी को मिली जान से मारने की धमकी, तीन गिरफ्तार&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">इंस्टाग्राम पर नुपुर शर्मा की तस्वीर डालने पर कारोबारी को मिली जान से मारने की धमकी, तीन गिरफ्तार</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नुपुर शर्मा की जीभ काटने पर 2 करोड़ रुपये इनाम देने की घोषणा करने का आरोपी गिरफ्तार&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नुपुर शर्मा की जीभ काटने पर 2 करोड़ रुपये इनाम देने की घोषणा करने का आरोपी गिरफ्तार</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नूपुर शर्मा को समर्थन : सोशल मीडिया कमेंट पर बिहार में भिड़े युवक, राजस्थान में वकील को मिली धमकी&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नूपुर शर्मा को समर्थन : सोशल मीडिया कमेंट पर बिहार में भिड़े युवक, राजस्थान में वकील को मिली धमकी</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;अजमेर दरगाह का खादिम गिरफ्तार, BJP की पूर्व प्रवक्ता नूपुर शर्मा को लेकर दिया था भड़काऊ बयान&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">अजमेर दरगाह का खादिम गिरफ्तार, BJP की पूर्व प्रवक्ता नूपुर शर्मा को लेकर दिया था भड़काऊ बयान</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>
    <tr style="height: 21px;">
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नुपुर शर्मा को धमकाने के आरोप में अजमेर दरगाह के मौलवी पर केस दर्ज&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नुपुर शर्मा को धमकाने के आरोप में अजमेर दरगाह के मौलवी पर केस दर्ज</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Pro Hindu&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Pro Hindu</td>
    </tr>


      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;नूपुर शर्मा को सुप्रीम राहत, देशभर में दर्ज सभी केस दिल्ली ट्रांसफर, SC का आदेश&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">नूपुर शर्मा को सुप्रीम राहत, देशभर में दर्ज सभी केस दिल्ली ट्रांसफर, SC का आदेश</td>
      <td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Neutral&quot;}" style="border: 1px solid rgb(204, 204, 204); overflow: hidden; padding: 2px 3px; vertical-align: bottom;">Neutral</td>
    </tr>
  </tbody>
</table></google-sheets-html-origin>


 <h3> Experimental Design </h3>
<p> We wrote the executable code for this project in Google Colaboratory Notebook which implemented Python 3.7 version. The flow of Python code includes
Hindi text pre-processing, exploratory data analysis of the collected dataset
and model construction and evaluation. </p>

<h3>Codes</h3>
<li><a href="https://github.com/TanyaChhikara/Detecting_Social_and_Politicla_Bias_in_Hindi_Media/tree/main/EDA" >Data Pre-processing and EDA</a><br></li>
<li><a href="https://github.com/TanyaChhikara/Detecting_Social_and_Politicla_Bias_in_Hindi_Media/tree/main/Web%20Scraping">Web Scraping</a><br></li>

 <h3> Pre-processing of Hindi Text </h3>
 
<img src="https://github.com/TanyaChhikara/Detecting_Social_and_Politicla_Bias_in_Hindi_Media/blob/main/Output%20Images/EDA_2.png" alt="Smiley face" height=auto>
<img src="https://github.com/TanyaChhikara/Detecting_Social_and_Politicla_Bias_in_Hindi_Media/blob/main/Output%20Images/EDA_3.png" alt="Smiley face" height=auto>

<h3> Model Construction </h3>
<p> N-gram Model Hyper-Parameter Tuning: It is observed that analysing the pattern of words frequently occurring in case of biased and unbiased data can yield better results. Therefore, for each label, the most common words (or clusters of words) have been extracted using n-grams (2-grams). Set intersection is performed for pro and anti labels to eliminate the words occurring in both sets. This resulted in an exclusive list of 2 grams for each label that displayed visible biases. Figures show the list of top10 words in the pro-BJP category and the list of top 10 words in the anti-BJP category. This approach was implemented in the construction of an n-gram model with hyper-parameter tuning using GridSearchCV. 5 different types of n-grams: unigram, unigram_bigram, bigram, bigram_trigram, trigram has been generated for the dataset. Random Forest classifier has been used with varying max_depth and min_sample_splits. The unigram_bigram vector has displayed the best accuracy and f1 score as shown in Table 3. This approach was used to analyze any existing patterns or relations that reflect any indication of a particular label. For the purpose of previously mentioned algorithms, earlier mentioned vectorisation techniques were only used.</p>

<h3> Results </h3>
Model training has been performed for social and political bias on 3 different areas: title, detail and concatenating both title and detail. Table 4 and 5 show
that, when compared to conventional methods, neural network-based solutions significantly outperform them. Compared to evaluating the entire article, considering just the title predicts bias with a hardly noticeable difference in accuracy. Additionally, we can see that simply concatenating the headline with the detail significantly improves accuracy in bias prediction.
<br>
<br>
<img src="https://github.com/TanyaChhikara/Detecting_Social_and_Politicla_Bias_in_Hindi_Media/blob/main/Output%20Images/Results_1.png" alt="Smiley face" height=auto>
<img src="https://github.com/TanyaChhikara/Detecting_Social_and_Politicla_Bias_in_Hindi_Media/blob/main/Output%20Images/Results_2.png" alt="Smiley face" height=auto>
<p>The best time complexity is 64.24% for political news and 57.99% for social news by logistic regression models. The above figures depict the train_test time complexities of different models on both political and social news data. For social bias, while considering only the title of the news as our dataset, the best accuracy among all the models is 52% (Random Forest) with an F1 score of 0.46 and considering only the news_description we get the best accuracy to be 52% with F1 score of 0.47 (Logistic Regression). However, the highest accuracy is achieved when both the title and description of news are taken together. The accuracy for the same is 57.99% with an F1 score of 0.55 (Lo- gistic Regression). Therefore, one can say that Logistic Regression is a better predictor in predicting social bias when it comes to either considering both news_title and news_description or just the news_description, and Random Forest performs best when we consider just the news_title.

For political bias, while considering only the title of the news as our dataset, the best accuracy among all the models is 54.92% (Logistic Regression) with an F1 score of 0.51 and considering only the news_description we get the best accuracy to be 63.73% with F1 score of 0.59 (Support Vector Machines). However, the highest accuracy is achieved when both the title and descrip- tion of news are taken together. The accuracy for the same is 64.24% with an F1 score of 0.59 (Logistic Regression). Therefore, one can say that Logis- tic Regression is a better predictor in predicting political bias when it comes to both news_title and news_description taken together and when consid- ering just the title,whereas, SVM performs best when we consider just the news_description.
</p>

<h3> Conclusion </h3>
<p> In this paper, we have first extracted news articles for various events from different news channel websites: NDTV News, The Quint and Zee News to propose a dataset for further model training. Major events that our re- search includes are Kisan Andolan, Hijab Controversy, Money Laundering, and Nupur Sharma Controversy. After performing NLP on the Hindi Text using pre-trained NLP models like iNLTK and StanfordNLP, we also imple- mented N-grams and Hyper Parameter tuning where the unigram_bigram vector has displayed the best accuracy and f1 score. Further, we observed the highest performance was achieved by logistic regression which is outperform- ing our RNN model by a difference of 10%. As a part of future work, the model training needs to be focused on analyzing news articles based on news sources as well as political and social inclinations. This can be computed using Named Entity Resolution comprising different journalists, activists, political leaders, and parties. </p>
