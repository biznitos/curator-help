AI AGENT GENERATOR
==================

Many times you need to create a new post, 
but you need different content in different fields.
You can easily program the content generator to
automatically use a common context and 
answer questions to update specific fields.

FORMAT
------
THe format of your content is made up of directives and prompts or contextual information.
Directives are always on their own line.
Prompts or contextual information can make up any number of lines.

# DIRECTIVES:

**xxxx:yyyy:zzzz**
Context or Prompt

xxxx = "role" -- This must always be there. Can never have another value.
yyyy = "user" -- What this message is for. Values are either "system" or "user".
zzzz = "fieldname" -- The fieldname of the post you need to update. If no fieldname, put "none"

Example:
**role:system:none** <- This is the first directive and the next lines that follow must be either the context, or the prompt.

Example:
**role:user:description** <- Update the description field with the prompt below.

EXAMPLE
-------
role:system:none
You are a funny poet working for a business named Biznitos Ltd. 
You write in the style of William Sheakspare sonnets.
Here is the information I want you to remember for the next steps.
... what you want to write about (can be few pages of info) ...

role:user:title
Write a short click-bait title using alliterative style about this topic.
Must be at most 72 characters long.
Must be text only

role:user:content
Write the poem in the style of sheakspare's sonnet.
It should have 3 stanzas.
Must be funny and naughty.
Output in markdown format.

role:user:description
Summarize the topic above that will lead people to read the poem.
Must be at most 50 words.
Must be text only

role:user:meta1
Write a commentary no longer than 2 sentences about the poem you wrote.
It should be in text format.

ACTUAL EXAMPLE
--------------
role:system:none
You are a tour operator named Thai Kru. 
You provide services for people coming to Thailand. 
But these are not "normal" tours. 
These are services that help people to either relocate to Thailand, or stay here for an extended time.
You are also a marketing copywriter for this service.
Use the context below to generate any additional content.

CONTEXT:
Condo Touring/Home Search
Problems you might have
Where is the best area to live?
Hard to find the one fit your budget, preference and areas you like
What is the average price for a 1 bedroom condo I should expect?
Don’t truly understand and difficult to communicate because owner is the local, cannot speak English
Want someone to take you to see in person before deciding
What is a common element for a Thailand condo?
No idea of the rules rental lease in Thailand
How much deposit you need for the booking, initial price you need to pay
How can I pay the deposit?
Where to find good price furniture?
How to set up internet and WiFi services?
How safe of the area and the place
How to find pet friendly condos?
How to move your belongings to Thailand

List of things we will do
Personalized Property Search and Tour to fit your budget, preferences, and desired location.
Arrange virtual and in-person tours of potential properties to help you make a decision.
Provide Translation assistance with your landlord for smooth communication
Assist in checking the rental lease and explain rental lease rules and property ownership. General amount of Initial deposit and contract duration and payment method.
Assist with setting up essential utilities like internet and WiFI and mobile phones.
Help you find quality, affordable local amenities such as furniture that meets your need, school, hospital nearby,  grocery stores, and public transport
Provide how to be safe, what you should or should do
Assist with moving your belongings internationally to Thailand.

role:user:meta1
We are proving a service named "Condo Touring/Home Search". 
Given the list of problems people have with finding accommodation, 
write a short, impactful paragraph (at grade 6 level) of about 5 sentences
that encompass the main pain points in the second person in the context below.
Output in plain text.

role:user:content
Create a detailed and structured article that points out what the customer can expect to receive and how it addresses each of the pain points.
Use about 650 words.
Do not include a title.
Output in pure Markdown format with no other text.

role:user:meta2
Given what you already said, provide a simple bulleted list of the 4 most impactful things the customer would get.
Do not include a title.
Output in pure Markdown format with no other text.

role:user:description
Summarize this service with an inviting description of no more than 3 sentences at a grade6 level.
Do not include a title.
Output in pure text only format.

role:user:meta3
Provide a brief list of the top 6 kinds of customer this is best for. 
Give examples for each one - without repeating anything about the service. 
Do not include a title.
Output in pure Markdown format with no other text.

role:user:meta4
Given what you already said, Thai Kru requires booking for this service between 3 months and 3 days before the service date. We also require full payment as well. Write a couple of  friendly sentences for this booking requirement.
Do not include a title.
Output in pure text only format.%   
