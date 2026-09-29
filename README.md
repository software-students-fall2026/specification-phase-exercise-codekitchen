# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

See instructions. Delete this line and replace with a list of the names of your team members, including links to each one's GitHub profile.
Risha Chada - https://github.com/rishachada
Yufei Huang - https://github.com/yufeiihuang
Sanjana
Ryan
Selma

## Review of the Current Application

*** ADD TWO MORE PLS!!!

From our findings and testing of the product, we have identified the following features as a current strength, weakness, or gap in the Slide Machine.

Strengths:
1. Filters out filler words and clarifies speaker's words into short, concise sentences

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

Checked the project's Future Work, Open Questions, Roadmap, Specs doc, and pull requests. Did not find any mention of showing the written transcript as an added feature to improve student review.

## Stakeholders

See instructions. Delete this line and replace with the name(s) of the stakeholder(s) you interviewed and lists showing their goals/needs, and problems/frustrations. Note which type of user each stakeholder represents. You may use pseudonyms or partial names to maintain their privacy, but you must privately share their full names and contact information as part of your submission of this exercise

Instructors

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
9. As an instructor, I want to view the transcript of my lecture so that I can review what was captured from my spoken presentation.
10. As an instructor, I want to search my transcript for a word or phrase so that I can quickly locate where I discussed a topic.
11. As an instructor, I want to correct errors in the transcript so that the written version accurately represents my lecture.
12. As an instructor, I want to preview the lecture as a student would see it so that I can verify that the table of contents, slides, and transcript work together as intended.
13. As an instructor, I want to regenerate the table of contents after substantially changing my lecture so that it reflects the updated content.
14. As an instructor, I want to know when the table of contents or transcript is still being generated so that I know when my lecture is ready to review.
15. As an instructor, I want to be notified when generating the table of contents or transcript fails so that I can retry the operation or take another action.


User Type 1: Instructors

1. As a student, I want to view the lecture's table of contents so that I can understand what topics the lecture covers.
2. As a student, I want to select a topic from the table of contents so that I can jump directly to that part of the lecture.
3. As a student, I want the table of contents to reflect the topics actually covered in the lecture so that I can use it as a reliable study guide.
4. As a student, I want to view the lecture transcript so that I can read the lecture content instead of relying only on the audio.
5. As a student, I want to search the transcript for a keyword or phrase so that I can quickly find where a topic was discussed.
6. As a student, I want matching terms highlighted in the transcript so that I can quickly identify relevant passages.
7. As a student, I want to move between matches for my search term so that I can review each relevant part of the lecture.
8. As a student, I want to select a passage in the transcript and jump to the corresponding part of the lecture so that I can hear the instructor's explanation.
9. As a student, I want to see which section of the lecture I am currently reviewing so that I know where I am within the lecture.
10. As a student, I want to see my progress through the lecture so that I know how much of the material I have reviewed.
11. As a student, I want my lecture progress to be saved so that I can return to the lecture without losing my place.
12. As a student, I want to resume the lecture from where I last stopped so that I can continue reviewing without starting over.
13. As a student, I want to jump between sections using the table of contents so that I can review topics in whatever order is useful to me.
14. As a student, I want the transcript and lecture sections to correspond to one another so that I can understand which written content relates to each topic.
15. As a student, I want to know when the transcript is unavailable or still being generated so that I understand why I cannot use it yet.

## Activity Diagrams

See instructions. Delete this line and place images of your UML Activity diagrams here, each with the text of the user story it illustrates.

## Wireframes

See instructions. Delete this line and place your wireframe diagrams here, covering every new screen and every existing screen your proposal changes, for every type of user.

## Clickable Prototype

See instructions. Delete this line and place a publicly-accessible link to your clickable prototype here.

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
