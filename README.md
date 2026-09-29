# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

See instructions. Delete this line and replace with a list of the names of your team members, including links to each one's GitHub profile.
- Risha Chada - https://github.com/rishachada
- Yufei Huang - https://github.com/yufeiihuang
- Sanjana Chauhan - https://github.com/schauhans
- Ryan Lin - https://github.com/ryanwlin
- Selma Nahas - https://github.com/berrizy

## Review of the Current Application

From our findings and testing of the product, we have identified the following features as a current strength, weakness, or gap in the Slide Machine.

Strengths:
1. Filters out filler words and clarifies speaker's words into short, concise sentences
2. The Slide Machine is able to generate–in real time–diagrams, images, and visuals that would traditionally take the lecturer time to find on the internet
3. The Slide Machine allows the lecturer to upload seed material which gives the lecture some guidance and tells the app what kind of material the lecturer would like to see on the screen. The seed material is reflected in the slides that are generated. 

Weaknesses:
1. As a group, we noticed that the AI-generated slide structure in terms of headers and bullets vs paragraphs was undisciplined and disorganized. Random tangents and side topics received their own dedicated slide which led to very high quanity, low quality (sparse) slides.
2. Hard to guage the main points of a lecture from slides, even with seed material that breaks down everything to cover
3. The 2 "plus" buttons are confusing and so is the difference between "new project," "new lecture," and "import a lecture."
4. Imported lectures (ppt and google slides) are heavily distorted and visually unnappealing


Gaps:
1. A running transcript that is saved with the slides would be useful for students and professors reviewing the lecture. A transcript would also help professors edit the generated slides manually for accuracy and clarity.
2. It is confusing to figure out how to edit and customize settings for the seed-blended option. A tutorial of some sort would be helpful for new users.
3. There should be a warning that all uploaded material is public to NYU by default in case professors would like to protect their slides and do not realize the public leaderboard setting.


## Prior Art & Originality

See instructions. Delete this line and replace with a short statement of what your team checked (the project's Future Work and Open Questions, its roadmap, and its open issues and pull requests) and which parts of your proposal are original — new work not already specified, scheduled, or proposed by someone else.

https://github.com/bloombar/slide-machine/blob/better-faster/docs/SPEC.md

The existing Slide Machine supports speech-to-text transcription and allows instructors to edit the spoken transcript on an individual-slide basis. However, we did not find a centralized workflow for reviewing the transcript of an entire lecture before publication, nor a student-facing transcript interface for reading, searching, and navigating lecture content. Our proposal extends the existing transcript infrastructure by introducing a centralized instructor review workflow with AI-assisted error detection and a student-facing synchronized transcript that allows students to navigate directly between transcript passages and the corresponding lecture slides.

## Stakeholders

See instructions. Delete this line and replace with the name(s) of the stakeholder(s) you interviewed and lists showing their goals/needs, and problems/frustrations. Note which type of user each stakeholder represents. You may use pseudonyms or partial names to maintain their privacy, but you must privately share their full names and contact information as part of your submission of this exercise

**Instructors**

Spanish Professor (SP) - details disclosed privately, pseudonym SP will be used

Goals/Needs:
- SP has very thorough pre-made slides, but spends a lot of time updating material for pacing purposes and adding in visual elements
- Sometimes students struggle with a grammar/vocab topic more than expected, and generating practice problems (i.e. fill-in-the-blanks, matching, etc.) during class would help SP gauge comfort level before moving on
- Currently uses powerpoint and spends a lot of time reformatting things in google slides when the conversion is messy so SP can share with other instructors

Problems/Frustrations:
- Did not know how to use the Slide Machine in the slightest
- In a short practice lecture on the past perfect tense, done almost entirely in spanish with numerous questions and confusions raised, the Slide Machine generated slides fully in English for some reason. While they could be translated to Spanish, they are only editable in English
- For a Spanish prof, SP prefers students not to be able to translate her speech and slide content to English with the click of a button
- Initially, SP uploaded seed material (sample lecture slides used in-class), and the Slide Machine generated very sparse, one-sentence slides and omitted a lot of the explanation SP gave
- Then, in a second run, SP tried importing a lecture so it would only generate new slides, which worked slightly better but added on English words to her Spanish slides and didn't pick up student questions
- Language professors, by nature, must repeat themselves often so students can understand the material, so auto-translating the slides to English hinders learning in this case
- Biggest frustration seemed to be difficulty around the different functionality between importing lectures, uploading seed material, and creating projects, as well as the settings

Teaching Assistant (TA) - details disclosed privately, pseudonym TA will be used

Goals/Needs:

- TA prepares lecture slides by summarizing the main points from the professor's Google Colab notebooks, and lately has been pasting the notebooks into ChatGPT to pull out the main points. Spends about 30 minutes to an hour per lectureAs a TA, their main in-class role is answering student questions as they come up, but TA said that as a professor they would want to spend more time adapting material
- Often explains things verbally that would work better as visuals. For example, when covering a data frame and the group by function, TA would like to show a before-and-after of the data rather than just talking through it
- Would split content by concept first, with "less on a slide is more." A large concept would get its definition on one slide and an example on the next
- Saw real value in being able to import both the lecture attachments and the notebook, then speak through the material and have the Slide Machine respond to all of it ("It would save a lot of time")

Problems/Frustrations:

- Biggest frustration with making slides is keeping each one structurally varied so students stay engaged
- Slides were generated well after TA had stopped talking, so the lag made the tool feel less responsive
- It wasn't clear which generated slides matched which parts of what TA said
- When TA said "for example" while speaking, the Slide Machine didn't generate an example, picture, or visual to go with it
- Overall reaction was positive ("pretty cool"), but the gap between what was said and what was generated limited its usefulness

**Students**

Junior Student (JS) - details disclosed privately, pseudonym JS will be used

Goals/Needs:
- JS saw the app as more useful for professors than students ("I'm not a teacher, but it would be useful if I was a professor")
- As a student, JS values lecture slides that include definitions, photos, and diagrams, which are hard to capture from speech alone ("I don't think you can speak those")
- Wants a way to add photos directly to slides
- Wants a way to cut out things said during recording that aren't meant to be part of the lecture
- Wants a tutorial or overview of what the app can do; JS did not know the Slide Machine could generate images until told after testing

Problems/Frustrations:
- Was confused by the "Discover" section and what the names and slide decks were, but figured it out shortly after (section not clear enough)
- On the "Design Templates" page, assumed templates could be created, but only premade options exist (name is misleading)
- Found the template pages overcluttered with too many fields, describing them as "overstimulating to look at"
- Tried to make a slide from a selected template but couldn't figure out how and gave up; did not understand the "Export" or "Duplicate this Design" buttons
- Eventually found the + on the Home Page to create slides
- When testing with a seed description and speech, the Slide Machine misspelled JS's name and titled the slides "My Talking" based on her aimless talking ("Oh, do I just talk into it?"), showing a disconnect with user intention
- Struggled to find the log out button: it was not in the expected upper right corner, clicking the logo did not redirect to the main page, and JS eventually found it in the hamburger menu after some confusion

Senior Student (SS) - details disclosed privately, pseudonym SS will be used

Goals/Needs:

- SS didn't see much value in the app for students. He felt that if the professor is already presenting, the slides and audio don't add much ("you already know what you're going to say, so I don't really see the point")
- As a student, SS studies by reading slides start to end and noting key terms, often the bolded ones. He would not replay the audio ("I wouldn't use the playback at all")
- Wants a written transcript of the "Play Deck Aloud" audio so he can read it instead of re-listening ("I would definitely add a transcript")
- Wants all the information in one place instead of split between the slides and the audio
- Values accessibility. He pointed out that deaf or hard-of-hearing students, or anyone in a quiet space without earbuds, would struggle if the audio has information the slides don't ("this would really suck, honestly")
- Would rather see only his own decks, or decks he's viewed before, on the home screen instead of Discover
- Liked the translation and re-listen features, but suggested a disclaimer that technical terms may not translate accurately
- Preferred list view over the default layout

Problems/Frustrations:

- Accidentally clicked a presenter's name instead of the slide, which took him to a profile page instead of the deck
- Wasn't sure how to move through a deck. He almost pressed "Play Deck Aloud" when he only wanted to click through the slides
- The left and right arrows were hard to see when the viewer was small
- Found the "Play Deck Aloud" label misleading because it plays something other than the slide content
- With no transcript, it was difficult to see all the information in one place
- Found the Discover section cluttered and unrelated to him ("I think it's really too much")
- Generally dislikes auto-generated slides. He feels they show less effort and organization than slides prepared in advance
- Didn't see the point of upvoting and downvoting
- The share button didn't work

## Product Vision Statement

We will enhance The Slide Machine with structured lecture navigation and review features that allow instructors to organize and customize generated lecture content while enabling students to navigate, search, and track their progress through lectures using a generated table of contents and searchable transcript.


## User Requirements

User Type 1: Instructors
1. As an instructor, I want to generate a table of contents from my completed lecture deck so that the major topics are organized for students
2. As an instructor, I want the generated table of contents to identify the major topics covered in my lecture so that students can understand the structure of the material.
3. As an instructor, I want each table-of-contents heading to link to its corresponding section of the lecture so that students can navigate directly to a topic.
4. As an instructor, I want to review the generated table of contents before adding it to my deck so that I can make sure the topics accurately represent my lecture.
5. As an instructor, I want to edit a generated table-of-contents heading so that I can use terminology that is appropriate for my course.
6. As an instructor, I want to add or remove topics from the generated table of contents so that I can control which topics students see as the major sections of the lecture.
7. As an instructor, I want to reorder table-of-contents headings so that the organization reflects the structure of my lecture.
8. As an instructor, I want the table of contents to update its links when I change the order of my slides so that students are always taken to the correct section.
9. As an instructor, I want to review the transcript of my entire lecture in one place so that I can check what was captured from my spoken presentation without opening each slide individually.
10. As an instructor, I want to search the full lecture transcript for a word or phrase so that I can quickly locate where I discussed a topic.
11. As an instructor, I want AI to flag transcript passages that may have been transcribed incorrectly so that I can focus my review on potential errors.
12. As an instructor, I want AI to flag transcript passages that may not correspond to the content of the associated slide so that I can identify potential transcription or content issues.
13. As an instructor, I want to approve or dismiss AI-generated transcript warnings so that I remain in control of the final transcript.
14. As an instructor, I want to preview the lecture as a student would see it so that I can verify that the table of contents, slides, and transcript work together as intended.
15. As an instructor, I want to regenerate the table of contents after substantially changing my lecture so that it reflects the updated content.
16. As an instructor, I want to know when the table of contents or transcript is still being generated so that I know when my lecture is ready to review.
17. As an instructor, I want to be notified when generating the table of contents or transcript fails so that I can retry the operation or take another action.


User Type 2: Students

1. As a student, I want to view the lecture's table of contents so that I can understand what topics the lecture covers.
2. As a student, I want to select a topic from the table of contents so that I can jump directly to that part of the lecture.
3. As a student, I want the table of contents to reflect the topics actually covered in the lecture so that I can use it as a reliable study guide.
4. As a student, I want to show or hide the lecture transcript so that I can choose whether to read along while listening to the lecture.
5. As a student, I want the transcript to automatically follow the lecture playback so that I can see the words being spoken.
6. As a student, I want to search the transcript for a keyword or phrase so that I can quickly find where a topic was discussed.
7. As a student, I want matching terms highlighted in the transcript so that I can quickly identify relevant passages.
8. As a student, I want to move between matches for my search term so that I can review each relevant part of the lecture.
9. As a student, I want to select a transcript passage and jump to the corresponding point in the lecture so that I can hear the instructor's explanation of that passage.
10. As a student, I want the transcript to indicate which slide each passage corresponds to so that I can understand how the spoken explanation relates to the visual material.
11. As a student, I want the lecture to automatically move to the corresponding slide when I select a transcript passage so that I can navigate between the transcript and slides easily.
12. As a student, I want to see which section of the lecture I am currently reviewing so that I know where I am within the lecture.
13. As a student, I want to see my progress through the lecture so that I know how much of the material I have reviewed.
14. As a student, I want my lecture progress to be saved so that I can return to the lecture without losing my place.
15. As a student, I want to resume the lecture from where I last stopped so that I can continue reviewing without starting over.
16. As a student, I want to jump between sections using the table of contents so that I can review topics in whatever order is useful to me.
17. As a student, I want the transcript and lecture sections to correspond to one another so that I can understand which written content relates to each topic.
18. As a student, I want to know when the written (not audio) transcript is unavailable or still being generated so that I understand why I cannot use it yet.

## Activity Diagrams
1. Generate and review a table of contents
<img width="350" height="633" alt="Screenshot 2026-09-29 at 5 34 52 PM" src="https://github.com/user-attachments/assets/b3734639-a84e-4ef4-9dcf-2c286a14b8e1" />
2. Review the full lecture transcript
<img width="352" height="619" alt="Screenshot 2026-09-29 at 5 35 17 PM" src="https://github.com/user-attachments/assets/cf4b0757-70fe-4281-a41f-0fab01447d38" />
3. Navigate topics and resume progress
<img width="353" height="606" alt="Screenshot 2026-09-29 at 5 35 41 PM" src="https://github.com/user-attachments/assets/d9c52349-1550-43b5-88a9-dedd79e187af" />
4. Search and navigate the transcript
<img width="349" height="629" alt="image" src="https://github.com/user-attachments/assets/5786bc2d-f845-47c7-ba9d-0555dc642efd" />


## Wireframes

<img width="775" height="386" alt="Screenshot 2026-09-29 at 5 06 38 pm" src="https://github.com/user-attachments/assets/95272e30-7fbc-4c37-b857-453845e1eac6" />
<img width="748" height="530" alt="Screenshot 2026-09-29 at 5 02 10 pm" src="https://github.com/user-attachments/assets/431fc9ac-cd9b-4d75-9e2c-a6ea487af809" />

## Clickable Prototype

See instructions. Delete this line and place a publicly-accessible link to your clickable prototype here.

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
