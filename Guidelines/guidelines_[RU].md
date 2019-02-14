
# RuSentiment Post Sentiment Annotation Guidelines

- [Annotation tool interface](#head1)
- [Sentiment annotation](#head2)
- [Positive speach acts](#head3)
- [Posts that dont express sentiment](#head4)
- [Smileys](#head5)
- [Hashtags](#head6)
- [Mixed sentiment](#head7)
- [What to skip](#head8)
- [Training examples](#head9)


# <a name="head1"></a>Annotation tool interface

![annotation_interface](./img/tool_interface.png)

In order to use our web-interface, you will first complete a training. **Finish reading these guidelines before you proceed**.  You will receive links and credentials for accessing the interface from the coordinator.  You will be presented with a set of training posts that are pre-annotated; after you enter your annotation, you will see how they should in fact be annotated. If anything is not clear, please refer to these guidelines again.

# <a name="head2"></a>Sentiment annotation

In sentiment analysis, our goal is to isolate the feeling or attitude being conveyed through a post on social media. Some posts express an obvious positive or negative sentiment or attitude towards something, and we need to select such clear, unambiguous cases. 

The sentiment conveyed in text may refer to (1) the speaker’s subjective mood, feeling, or emotion, or to (2) the speaker’s attitude towards something.  For example:

| (1) Speaker mood/emotions | (2) Evaluation of an entity or event |
|---------------------------|--------------------------------------|
| Настроение поднялось:)) | Крутой фильм |
| Я счастлив | Котэ прекрасен. |

Both the speaker’s mood and their attitude towards something can be positive or negative:

<table class="tg" style="width: 652px;">
<tbody>
<tr>
<th class="tg-031e" style="width: 182px;">&nbsp;</th>
<th class="tg-031e" style="width: 227px;">Positive</th>
<th class="tg-031e" style="width: 233px;">Negative</th>
</tr>
<tr>
<td class="tg-031e" style="width: 182px;"> Emotions, mood of the speaker</td>
<td class="tg-031e" style="width: 227px;">
<p>happiness, pride, love, inspiration, serenity, interest&hellip;</p>
<ul>
<li>УРРРРААААААА!!!!!! )))</li>
<li>Туц туц туц!!! Я это сделала) Горжусь собой😃😎
</li>
</ul>
</td>
<td class="tg-031e" style="width: 233px;">
<p>sadness, anger, fear, hatred, pain, disgust, shame, guilt&hellip;</p>
<ul>
<li>НЕСУДЬБА повсюду
</li>
<li>господи как же скучно вконтакте. что я здесь делаю?</li>
</ul>
</td>
</tr>
<tr>
<td class="tg-031e" style="width: 182px;">Evaluation, attitude towards some entity or event</td>
<td class="tg-031e" style="width: 227px;">
<ul>
<li>годный дабстеп, очень годный.</li>
<li>Умничка,очень рада за тебя.</li>
<li>Обожаю людей, которые пишут - звонят, просто так, чтобы пообщаться, узнать как дела...
</li>
</ul>
</td>
<td class="tg-031e" style="width: 233px;">
<ul>
<li>БЛИН, КАКИХ ТОЛЬКО КОНЧЕНИХ ЛЮДЕЙ МИР НОСИТ...!!!
</li>
<li>Неудачные кадры</li>
<li>Мозг отсутствует.</li>
<li>я не держу на ниё зла-пускай идет с миром...но на хуй</li>
<li>удивительный отстой</li>
</ul>
</td>
</tr>
</tbody>
</table>

All of the above cases (whether they deal with the speaker’s emotions/mood or evaluation/attitude) are cases of explicit sentiment - you can tell the sentiment because it is clearly stated in the post. However, in many cases the sentiment may be implicit - you can understand how the speaker feels or what his/her attitude towards something is, but it is not expressed directly. Cases of implicit sentiment include: 

<table class="tg" style="width: 637px;">
<tbody>
<tr>
<th class="tg-l711" style="width: 137px;">&nbsp;</th>
<th class="tg-l711" style="width: 229px;">Positive</th>
<th class="tg-l711" style="width: 259px;">Negative</th>
</tr>
<tr>
<td class="tg-l711" style="width: 137px;">Wishing (or not) for something, recommendations<br /><br />EVALUATION IS IMPLIED</td>
<td class="tg-l711" style="width: 229px;"><br />
<ul>
<li>Хочу снега. Много-много. Чтобы снежки и снеговики. И ночью все светится!!!
</li>
<li>Осень осень, подари мне ауди R8</li>
<li>Всем бы таких поклонниц</li>
<li>Обязательно попробуй шампусик</li>
<li>рекомендует фильм «Подмена» (2008)</li>
</ul>
</td>
<td class="tg-l711" style="width: 259px;">
<ul>
<li>Ааааа не хочу учиться:( </li>
<li>Не дай бог к такому преподу попасть</li>
<li>Не пытайся даже это есть, все равно вырвет</li>
</ul>
</td>
</tr>
<tr>
<td class="tg-l711" style="width: 137px;">Descriptions of experience that most people would consider positive or negative<br /><br />EMOTION IS IMPLIED</td>
<td class="tg-l711" style="width: 229px;">
<ul>
<li>мы победили!</li>
<li>Посмотрела с удовольствием.</li>
<li>Я получил премию!!</li>
</ul>
</td>
<td class="tg-l711" style="width: 259px;">
<ul>
<li>сломала каблук. попала под дождь. порвала чулок.....</li>
<li>Блядократия победила</li>
<li>15 дней к окончанию сессии...
</li>
</ul>
</td>
</tr>
<tr>
<td class="tg-l711" style="width: 137px;">Questions with clear implicit sentiment (often rhetorical)<br /><br />EMOTION is IMPLIED</td>
<td class="tg-l711" style="width: 229px;">&nbsp;</td>
<td class="tg-l711" style="width: 259px;">
<ul>
<li>Вот как я теперь её найду?(((</li>
<li>Iван, а почему так строго и недоверительно?</li>
<li>Не понимаю почему я постоянно сонная!?</li>
</ul>
</td>
</tr>
</tbody>
</table>

Unfortunately, it is not always the case that a whole single post fits one of the above categories. If the post contains several expressions of sentiment, we ask you to annotate the polarity of the post as a whole, which we define as the **dominant, prevailing sentiment**. Annotation of the mixed sentiment posts is discussed below (such as the posts containing both positive and negative sentiment) is discussed [here](#head4).

Posts may express sentiment of two different types, for example, the speaker's mood and the speaker's attitude towards something.  The polarity of these may be the same or it may differ, creating a mixed-sentiment post.  Often, the polarity will be the same.  For example, “круто! Выиграла бесплатный билет” has both an explicit evaluation of the event (круто!) and describes the experience that would be positive for many people (Выиграла бесплатный билет). It is clear that the polarity of the post as a whole is also positive.

# <a name="head3"></a> Positive speech acts

A large portion of posts express perform the functions of various speech acts: expressing gratitude for something, congratulating a user or a group of users, greeting them. We treat these as a separate subcategory because, although generally greetings, congratulations and gratitude imply positive sentiment, they can also be performed, e.g., out of a feeling of obligation or under social pressure. So we would like to keep it an option to add or remove them in different research scenarios.

This group includes: 

**Expressions of gratitude:**
- Спасибо Алён за поздравления! очень приятно!! когда сезон открывать будем?)))
- Всем спасибо за поздравления! :)
- "Особая благодарность эльфу-торговцу"!

**Congratulations:**
- С ДНЕМ ВАРЕНЬЯ!!! Вечного Творческого Возбуждения )) ... стабильного здоровья ;)
- И тебя с Наступающим Днём Ангела;)
- Эту девушку я дарю тебе, С ДР!!

**Good wishes to someone:**
- Желаю всем удачи в ЗНО по математике!!! Напишите все на 200 баллов)))))

**Greetings:**
- С добрым утром!
- Приветик) как ты? Ты в Киеве?
- всем весна, пасаны

If there is clear irony, treat these as cases of mixed sentiment.

# <a name="head4"></a>Posts that don't express sentiment

"No sentiment” label is reserved for **posts that simply describe some situation in a neutral, matter-of-fact way**, and have no clear positive or negative sentiment. For example:</div>

- первый запуск няши разрешением 720p (800 на самом деле) <span style="float:right;"> [no sentiment]</span>
- Вареные мидии с рисом и перцем.  <span style="float:right;"> [no sentiment]</span>
- знакомая девочка <span style="float:right;"> [no sentiment]</span>

The same label applies to most **matter-of-fact, non-rhetorical questions**:
- где бы теперь взять экран 3х2 метра <span style="float:right;"> [no sentiment]</span>
- Что у вас нового?? <span style="float:right;"> [no sentiment]</span>
- Кто в Москву с сурикатами? =) <span style="float:right;"> [no sentiment]</span>

If the post carries no overall sentiment, but is followed by smileys, please use the “no sentiment” label. For example:
 - Первый, и последний раз))) <span style="float:right;"> [no sentiment]</span>
 - Я вернулся) <span style="float:right;"> [no sentiment]</span>

Other categories of posts that should be annotated with “no sentiment” label include:

**(1) Advertisements:**

- куплю 1 нефть <span style="float:right;"> [no sentiment]</span>
- В мою компанию требуется руководитель Удостоверяющего Центра. Электронные аукционы, выдача ЭЦП, РоссАлкогольРегулирование, ФСТ.  Образование высшее. Опыт работы может быть не большим...Резюме в личку Телефон в профиле <span style="float:right;"> [no sentiment]</span>
- Всем кому интересны подробности и новости проекта, приглашаю подписаться на сообщество!) Идея в максимальной автоматизации ухода за домашними растениями с управлением и мониторингом параметров среды через интернет с любого устройства) <span style="float:right;"> [no sentiment]</span>

**(2) Professional plot summaries of movies, books, etc:**

- Действие фильма развернется в одном из глухих сибирских поселков. Юный главный герой по имени Колыма оказывается впутан в жестокий криминальный мир своего родного городка. Мы увидим становление этого мальчика, которому приходится принять правила их общины и пуститься во все тяжкие...(Малкович) <span style="float:right;"> [no sentiment]</span>

**(3) Requests for information:**

- Такой вопрос. Если заказываешь вещь, а доставляют ее через неделю,скажем, по какому курсу платить? Дня заказа или дня доставки? Ответьте,пожалуйста, в личку. <span style="float:right;"> [no sentiment]</span>

Neutral posts do not necessarily contain full clauses. For instance, they may be titles or descriptions of media or files attached to а post:

- "Самолет с крыльями и окнами" <span style="float:right;"> [no sentiment]</span>
- Тесты по математике, ГИА-2011, 9 класс <span style="float:right;"> [no sentiment]</span>

# <a name="head5"></a>Smileys

An important caveat concerns smileys. We distinguish 3 cases:

**1. smileys are the ONLY indication of any sentiment.**

- Нужна...просто так))) <span style="float:right;"> [no sentiment]</span>
- Папарацци не дремлют!)))) <span style="float:right;"> [no sentiment]</span>

Such posts should be annotated with the**“no sentiment" label**, because the smileys here are used to simply mimic the facial expressions in a normal face-to-face conversation rather than express strong sentiment. Besides, they are easy to detect automatically. 

**2. smileys MIRROR the sentiment expressed verbally:**

- Покатался =))) доволен, хочу еще! <span style="float:right;"> [positive]</span>
- Победа - ценой руки((<span style="float:right;"> [negative]</span>

Such posts should be annotated to **reflect the sentiment expressed verbally.**

**3. smileys CHANGE the sentiment expressed verbally:**

- )))))))Плохой санта))<span style="float:right;"> [positive]</span>

In such cases **the overall dominant sentiment should be annotated**. The smileys weaken the explicit negative evaluation in bad/awful, they indicate that the speaker is joking. The overall sentiment is positive - although it is only expressed by the smileys.

**4. smileys HEDGE the overall sentiment, usually serving to make negative sentiment sound slightly less negative, but not completely reversing the sentiment.**

- Ну блин начало сессии:)))) всю группу так конкретно завалить...:)))<span style="float:right;"> [negative]</span>

In these examples, the smileys weaken the explicit negative evaluation, but the overall sentiment is still negative.

Unlike smileys, words indicating mood (laughter, cries, swearing etc.) should always be taken into account.

 - Бро, как тебе ? ахахах <span style="float:right;"> [positive]</span>

Abbreviations like LOL and OMG should also be taken into account.

# <a name="head6"></a>Hashtags

Hashtags are generally treated as information units, similarly to words. The following example should be annotated as positive because both \#выпускной and \#на пляж are generally positive experiences:

- На пляж по традиции :) #выпускной #prom <span style="float:right;"> [positive]</span>

On the other hand, similarly to words, they are to be ignored if the post consists entirely of hashtags and was probably accompanying some picture or video, and is uninterpretable without that content.

- \#крымнашбожехранироссею
- \#пары\#вседела

However, some hashtags explicitly express the speaker's mood or evaluation. In such cases, they should be treated accordingly, similarly to happy or terrible.

- \#Дима_возмущается \#Недовольство <span style="float:right;"> [negative]</span>
- YOUTUBE ввел нововведение: теперь видеохостинг не отображает просмотры, собранный роликами на сторонних сайтах. #мнененравится<span style="float:right;"> [negative]</span>

# <a name="head7">Mixed sentiment

Some posts contain both positive and negative sentiment words, and are therefore usually more difficult to annotate. In these cases, our policy is to annotate the **DOMINANT SENTIMENT** expressed in the post. That is, if you feel that overall the feeling expressed in the post is positive, it should be annotated as such (and vice versa).  

For example, in the following example we have both positive and negative sentiment:

- Почему Женя не выбрал нашу Ирочку ?! да потому  знает что недостоин,  жить с такой красивой, умной, состоятельной, самоуверенной девушкой ! =))) <span style="float:right;"> [positive]</span>

While “Женя не выбрал нашу Ирочку” could be a negative experience for the girl in question, it is outweighed by the positive evaluation of the her.

- Каникулы подошли к концу...Это были самые лучшие,незабываемые каникулы...У меня никогда не было такого колличества светлых впечатлений, эмоций, позитива! Таня, Катя, Егор, Андрей, Вася, Коля, Алиса-спасибо Вам!!! Вы лучшие!!!:) <span style="float:right;"> [positive]</span>

This post also contains a negative experience (Каникулы подошли к концу...), but it is also clearly outweighed by the positive evaluations that follow.

The policy for some of the less clear cases is outlined below.

1. **irony, sarcasm** - overall negative entity is described with positive words:

- Замечательный день сегодня. То ли чай пойти выпить, то ли повеситься. <span style="float:right;"> [negative]</span>
- о дааа, 3 выходных, а я дома с ролтоном тусую... !! <span style="float:right;"> [negative]</span>

2.  **a negative characterization of some positive viewed entity, perhaps as a friendly joke:**
- вот такое хитрожопое чудовище у нас выросло и ест наш мозг )) <span style="float:right;"> [positive]</span>
- плохой санта :))) <span style="float:right;"> [positive]</span>

3. **an “acknowledging” characterization:** the speaker says that overall, something is good or bad but it has some drawbacks or advantages:

- Старый, но вечно доставляющий, всегда актуальный баян))<span style="float:right;"> [positive]</span>
- Операция на колено прошла успешно  )немного болит нога, а так все хорошо ,только скучно <span style="float:right;"> [positive]</span>

A frequent case of such a mixture is something positive happening **despite negative factors**:

- У меня такой х***вый характер...а ты терпишь. Спасибо.<span style="float:right;"> [positive]</span>

Another possibility is that the positive/negative attitude towards something is situational and differing from the usual speaker's attitude. It is the given context, some specific circumstances that change the overall evaluation. For example:

- Вы не подумайте, что я люблю Америку... скорее наоборот, но..... <span style="float:right;"> [positive]</span>


4. **comparative evaluation:** something characterized as good or bad in comparison to something else:

- Когда учишь Бетховена, понимаешь, что Бах был довольно таки милым
композитором..... <span style="float:right;"> [negative]</span>

The speaker’s implication here is that Beethoven is so bad that even Bach is ok in comparison (although Bach is also bad without Beethoven as a reference point). In such cases, the attitude towards the “main entity” rather than the reference point should be annotated.

5. **double sentiment of the same subject:** the same segment may express both how a speaker feels and their attitude towards something, and it may differ. For example:

- Я по тебе скучаю. <span style="float:right;"> [negative]</span>
- Мне бы такую работу! <span style="float:right;"> [negative]</span>

In both of these cases the speakers express a high opinion of something, but they feel bad for not having it. In such cases, the speaker's mood towards something should be annotated as the main sentiment, not their attitude towards something.

6. a greeting or some other **speech act added to an overall neutral, informational post**:

- Всем​ ​желаю​ ​здравствовать​ ​!​ ​Выясняется потребность/интерес в механах из боевых бакелитовых корпусов 5,45 и 7,62, варианты для М серии...Если не трудно поделитесь опытом перепила или использования если таковой имеется.  <span style="float:right;"> [no sentiment]</span>

# <a name="head8">What to skip

We are interested in **CLEAR** cases of positive or negative sentiment, so, **IF IN DOUBT - SKIP IT!** This especially concerns descriptions of experience that would be positive or negative for the annotator personally, but not necessarily for most people.

Posts to skip include the ones in which:

(1) **The original meaning is impossible to ascertain without context (maybe because they were accompanied by photos, videos, or posted as replies to other posts):**

- Вчера/сегодня
- К чертям осьминогов, Бобик из Харькова никогда не ошибается!!!

**(2) The sentiment of the post as a whole is not entirely clear:**

- А завтра с утра опять изменю кровати с душем. Мудак.
- вот это, блять, работа!
- Это моя святая святых))) Незяяяяяя
- Своих друзей не выбираю И полагаюсь лшь на сердце. Я в душу дверь не закрываю, Впущу, кто захотел согреться.  Кто появился без корысти, Без кривотолков и без злобы, С открытою душой и чистой, За словом искренним и добрым.  Они поймут меня любую, И примут все мои причуды, Мы вместе, трудности минуя, Ещё родней и ближе будем.  И друг за друга мы готовы, Вступиться, если обижают, Оружие одно лишь - слово, Мы им богатство измеряем.

**(3) Languages other than English (e.g Ukrainian, Russian) are used:**

- Курва МАТЬ!!!! ШЕ 7 днів!!! Віпппіііііі)))))))
- hair: Irina Skochko, make-up: Anna Kuzminykh
- Ну а чим ще можна займатися, коли хворієш?))))

**(4) Jokes**

While jokes do imply positive mood of the user who shared them, identifying them is beyond the scope of this annotation task.  Therefore the jokes should be skipped.

- Минобороны закупает бадминтонные ракетки и воланы
Если жизнь тебя ебет, Значит у нее встает, Значит, ты ей нравишься! Так чего ты паришься?!)))
выпал зубик? не беда нам поможет- ПВА

# <a name="head9">Training examples

These pre-annotated examples were presented to annotators for training, before they proceeded to actual annotation. They got feedback on whether their label was correct, and also the reasoning behind the label that is shown below.

|  | Post |Label  | Feedback shown to the annotators |
|------|------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Блестай на страницах мира, детка!!!! | + | The speaker explicitly expresses their belief in the high ability of the addressee. |
| 2 | как жизнь? зато мухам нравится... | - | This is also negative sentiment of the speaker, but implicit, because there are no explicit sentiment words. |
| 3 | братановские розовые крепы решают! ) | Skip | This post is hard to interpret out of context. |
| 4 | Котлеты без мяса (сыроедческие) :: Вторые | No sentiment | This post just describes a situation without any sentiment |
| 5 | Хочу мяса с лавашом | + | Wanting or wishing for something implies a high evaluation of it, which is annotated as positive sentiment. |
| 6 | эээйййй....настроение....вернись.... | - | This is implicit sentiment, because the inner feelings of the speaker is described directly (although metaphorically) |
| 7 | С наступающим Новым Годом! Желаю всего самого наилучшего в грядущем году!)) | Speech-act | Congratulations, as well as greetings and expressions of gratitude should be annotated as speech-acts. |
| 8 | еще долго буду скучать по тебе... | + | Mixed explicit sentiment: the speaker has high esteem/love for someone, although their absence makes them feel bad. According to the guidelines, the dominant sentiment should be annotated, and in this case the sadness is outweighed by love. |
| 9 | Вконтакту грозит смерть. | - | This is implicit negative sentiment: the speaker shares news that he/she believes to be bad news for many people |
| 10 | Еду во Францию ))| + | This is implicit sentiment: the speaker shares an experience that most people would consider positive |
| 11 | 1030 дней вконтакте| No sentiment | The speaker simply states a fact |
| 12 | не понимаю, как у него язык повернулся такое сказать??? | - | This is a rhetorical question implying negative sentiment towards the target: the speaker their belief that people normally should not act as the target did. |
| 13 | неплохое будущее, говорите? АХАХАХАХ | - | This is mixed sentiment, specifically sarcasm: the speaker uses positive words to describe an entity that is actually evaluated negatively. |
| 14 | ФАК ФАК ФАК!!!завтра два модуля!!!начались модули забилось на пары))гггг  | - | This post contains both explicit and implicit sentiment: explicit emotion word (f*k), and also implicit emotion via sharing an experience that makes the speaker feel bad.  |
| 15 | Новое видео ждите на днях :Р | No sentiment | The speaker shares a piece of information |
| 16 | Блядократия победила | - | This is implicit negative sentiment: the speaker shares an experience that would make most people feel bad |
| 17 | вообще с ума посходили | - | This is explicit negative sentiment: we don’t know the mood of the speaker exactly, but he/she clearly states his/her opinion about the target|
| 18 | Разминка для мозга. Наслаждайтесь! | + | This is explicit sentiment: the speaker directly expresses his/her belief that the target would be appreciated by others |
| 19 | Полюбляю смакоту😜😜😜   | Skip | This post is not in Russian |
| 20 | иногда хочетса быть кому-то нужной,чтобы подошол любимый человек обнял крепко, крепко и сказал что все будет харашо я с тобой. | + | Wanting or wishing for something implies a high evaluation of it, which is annotated as positive sentiment. |
| 21 | Я: кошки, эппл, корки не oставляю, чай, стол (хотя бывает..), 50 кг, меню - по настроению)) | Skip | This post is hard to interpret |
| 22 | Эхо войны 🚨 | No sentiment | This is a matter-of-fact statement, probably describing some posted media. |
| 23 | знаю, что идиотски, но весело))) | + | This is mixed sentiment: the speaker expresses an overall positive evaluation of something, although it has some negative aspects. |
| 24 | Вот бы махнуть в Москву на дерби))) | + | This is implicit sentiment: the speaker expresses wishing for an event, which implies positive aspects. |
| 25 | Масяяяяяя)))) | Skip | This post is hard to interpret |


