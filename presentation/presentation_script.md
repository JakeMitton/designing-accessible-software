# Accessibility in Software Design — Video Script

---

## Slide 1: Title Slide

**Slide content:** Title — *Accessibility in Software Design*, your name, course/institution info

**Script:**

Hi everyone. My name is Jake, and today we are going to be talking about designing accessible software. Specifically, we will cover what accessibility means in the context of technology, why it matters, what the relevant standards are, and what you can actually do as a developer to make your software more accessible. Accessibility is a topic that often gets treated as an afterthought during development, and one of the goals of this video is to push back on that and make the case that it needs to be part of your process from the very beginning. So, let's begin.

---

## Slide 2: What is Accessibility?

**Slide content:** Definition — *Accessibility is about making resources equally available to users with disabilities or barriers to use.*

**Script:**

Alright, what do we actually mean when we talk about accessibility? At its core, accessibility is about ensuring that resources, whether that's a building, a document, a service, or a piece of software, are equally available to people who have disabilities or face other barriers to use.

When we talk about barriers, we're talking about anything that prevents a person from being able to fully use or access something. In a physical space, a curb without a ramp is a barrier for someone using a wheelchair. In the digital world, an image with no description is a barrier for someone using a screen reader. The concept is the same in both cases. We are asking: who might be excluded from using this, and what can we do about it?

It is also worth noting that accessibility is not just about permanent disabilities. Someone might have a permenant disability, a temporary injury that changes how they interact with technology, or be in an environment that limits how they can use a device, like a loud room where audio is not an option. Accessibility accommodates all of these situations.

---

## Slide 3: What Does Accessibility Mean for Software?

**Slide content:** Key idea — *Accessibility needs to be built in from the start, not added on later.* Example features: alt text on images, keyboard navigation.

**Script:**

Now let's narrow that down to software and digital content specifically. When we talk about accessible software, we mean software that has been designed and built in a way that ensures all users, regardless of disability or barrier, can access and use it effectively.

The key phrase there is "designed and built." Accessibility is not something you bolt on at the end of a project. It needs to be considered during requirements gathering, during design, during development, and during testing. We'll come back to this idea near the end of the video.

Some common examples of accessible features in software that you may have already encountered include alternative text on images, which is a short text description that a screen reader can read aloud for a user who is blind or has low vision; keyboard navigation, which allows a user to move through an entire interface using only the Tab key without ever touching a mouse; and captions on video content, which display spoken audio as text on screen. These might sound like niche features, but subtitles alone are used by millions of people without hearing difficulty at all, which is something we will come back to shortly.

---

## Slide 4: Why Should You Care?

**Slide content:** Accessibility benefits everyone. Example: subtitles are an accessibility feature widely used by people without hearing difficulties. Legal stakes: Accessible Canada Act, complaints, reputational risk.

**Script:**

At this point you might be thinking, how many users does this actually affect? And the honest answer is, more than you would think, and also, that framing misses the bigger picture.

According to the World Health Organization, over a billion people worldwide live with some form of disability. That's a significant portion of any potential user base. But beyond the numbers, there is a concept sometimes called the curb cut effect, which refers to the way that features designed for people with disabilities often end up benefiting everyone. The name comes from curb cuts in sidewalks, which were designed for wheelchair users but are used constantly by people with strollers, delivery carts, cyclists, and so on.

Subtitles are a perfect example of this in the digital world. Subtitles exist as an accessibility feature so that users who are deaf or hard of hearing can follow along with video content. But they are incredibly widely used by people without any hearing difficulty at all. If you have ever watched a video on your phone with the sound off, on a bus, or in a waiting room, and relied on the subtitles to follow what was happening, you have benefited from an accessibility feature. TikTok auto-captions are a great real-world example of this exact thing.

Beyond the ethical case, there is also a legal and organizational one. In Canada, the Accessible Canada Act creates enforceable accessibility obligations for federally regulated organizations, and complaints about inaccessible digital products can be filed with the Accessibility Commissioner. Beyond federal law, organizations that fail to meet accessibility standards face real reputational risk and potential liability. For a product you are building professionally, inaccessibility is not just a UX problem, it is a business and legal exposure. So accessibility is not just an ethical obligation. It makes your software better for everyone, and it protects the organizations that build and use it.

Source for WHO figure: who.int/news-room/fact-sheets/detail/disability-and-health
Source for Curb Cut Effect: https://www.policylink.org/resources/commentary/curb-cut-effect

---

## Slide 5: Does Accessibility Cost More?

**Slide content:** Honest acknowledgment: yes, accessibility adds development cost. But: building it in from the start costs less than retrofitting. Wider user base. It gets easier with experience. Co-designing helps.

**Script:**

Before we go any further, I want to be transparent about something. Incorporating accessibility into your software does add cost. It takes additional time to learn the standards, to implement things correctly, to test with assistive technology, and to involve users with accessibility needs in your process. That is real, and it would not be fair to talk about why you should care about accessibility without acknowledging it honestly.

That said, there are several things worth keeping in mind that put that cost in perspective.

The first is timing. Building accessibility in from the beginning of a project costs significantly less than trying to add it at the end. If you have already built an interface without considering keyboard navigation, going back and retrofitting it is expensive and often messy. If you consider it during design and development, the decisions that produce an accessible interface are often not much more work than the decisions that would have produced an inaccessible one. We mentioned this in the previous slide, and it is worth repeating here: the cost argument is actually one of the strongest reasons to treat accessibility as a design requirement from day one rather than a post-launch checklist item.

The second is reach. Accessibility widens your potential user base. The over a billion people worldwide living with disabilities represent real users your product could serve. Inaccessible software excludes them entirely. From a product perspective, the cost of making something accessible can often be recouped simply by not locking out a significant portion of your potential audience.

The third is that it gets easier. The first time you think carefully about keyboard navigation or colour contrast or screen reader compatibility, it takes real effort. The second time, less so. Developers who work with accessibility regularly describe it becoming part of how they think about interfaces from the start rather than a separate concern to address afterward. The upfront learning investment pays forward into every future project you work on.

Fourth, learning to design with accessibility in mind tends to reveal barriers you didn't even know existed. When you work through how a screen reader user experiences your interface, or how someone with limited motor control navigates a form, it changes how you think about interface design more broadly. Most developers who go through that process find it genuinely shifts their perspective.

Finally, co-designing with users who have accessibility needs, which we'll talk about more near the end of this video, can actually make the process easier rather than harder. People with lived experience using assistive technology can quickly identify the most significant barriers, which helps you focus your effort where it matters most rather than trying to anticipate every possible issue from the outside.

---

## Slide 6: What is Assistive Technology?

**Slide content:** Definition of assistive technology, examples: screen readers, braille displays, switch devices.

**Script:**

Before we get into the standards, let's take a moment to talk about assistive technology, because the standards we're going to cover are largely written around ensuring that software works correctly with it.

Assistive technology, often abbreviated as AT, refers to any hardware or software used by people with disabilities to help them interact with technology or the world around them. Some common examples are as follows.

Screen readers are software applications that read the content of a screen aloud. They are used by people who are blind or have low vision, and they work by interpreting the structure and content of an interface and converting it to synthesized speech or braille output. NVDA and JAWS are popular screen readers on Windows, and VoiceOver is built into Apple devices.

Braille displays are physical devices that connect to a computer and translate text on screen into braille that a user can feel with their fingertips.

Switch devices are input devices used by people who have limited motor control and cannot use a standard keyboard or mouse. They might be a single button, a sip-and-puff device controlled by breath, or eye-tracking software. These typically work by cycling through options on screen and selecting when the right one is highlighted.

The reason this matters for developers is that your software needs to be built in a way that assistive technology can interpret and interact with. If your interface cannot be parsed by a screen reader, or cannot be navigated without a mouse, users who depend on assistive technology are effectively locked out. The standards we're about to discuss exist to prevent exactly that.

---

## Slide 7: The Standards Landscape

**Slide content:** Two main standards: WCAG (Web Content Accessibility Guidelines) and EN 301 549 V3 (European Standard). Accessibility Canada has legislated EN 301 549 V3 federally.

**Script:**

Now let's talk about the standards that define what accessible software looks like in practice. There are two main ones you need to know about.

The first is the Web Content Accessibility Guidelines, or WCAG. This is the primary international standard for accessible web development. It is developed and maintained by the World Wide Web Consortium, the W3C, through their Web Accessibility Initiative. WCAG is what most developers are referring to when they talk about web accessibility standards.

The second is EN 301 549 Version 3, which is a European standard that takes a broader view. It covers accessibility requirements for software beyond just the web, including native applications, operating systems, and hardware. Importantly, version 2.1 of WCAG is incorporated into EN 301 549 V3, so the two standards are closely linked.

In a Canadian context, Accessibility Canada has legislated the use of EN 301 549 V3 as the federal standard for accessibility through the Accessible Canada Act. This means federally regulated organizations in Canada are expected to meet these requirements. So even if you're not building something for the European market, this standard is directly relevant to work done here.

We're going to spend most of our time looking at WCAG in detail, since it is the most directly applicable standard for web developers, and then we will cover what EN 301 549 adds on top of that.

---

## Slide 8: WCAG — The Four Principles (POUR)

**Slide content:** WCAG's goal: make web content **Perceivable, Operable, Understandable, and Robust** (POUR). Quick reference link: https://www.w3.org/WAI/WCAG22/quickref/?versions=2.1

**Script:**

WCAG is organized around four core principles. You can remember them using the acronym POUR: Perceivable, Operable, Understandable, and Robust. Every success criterion in WCAG maps back to one of these four principles.

Before we go through each one, I want to flag a useful resource. The W3C maintains a quick reference guide for WCAG 2.1, the link for which is on the resource page. If you are working on a web project and want to check your work against the standard, that's the place to go. You can filter by principle, guideline, and conformance level.

Now, let's go through each principle one by one.

---

## Slide 9: Perceivable

**Slide content:** *Information must be presented in a way users can perceive, through at least one of their senses.* Four areas: Text Alternatives, Time-Based Media, Adaptable Content, Distinguishable.

**Script:**

The first principle is Perceivable. This means that all information and interface components must be presented in a way that users can actually perceive. In other words, they need to be able to process it through at least one of their senses. If someone can't see an image, they need another way to access that information. If someone can't hear audio, they also need an alternative. Perceivability is about ensuring no information is locked behind a single sensory channel.

WCAG breaks perceivability down into four areas.

The first is Text Alternatives. Any non-text content, including images, icons, and buttons that use pictures instead of words, should have a text alternative. The most common example is alt text on an image tag in HTML. A screen reader will read that alt text aloud to a user who cannot see the image. If your image is purely decorative, you can use an empty alt attribute to tell the screen reader to skip it. But if the image conveys information, like a chart, a diagram, or a photograph with meaningful content, that information needs to be described in text.

The second area is Time-Based Media. Videos and audio content need alternatives. For video this means captions, text that appears on screen synchronized with the spoken audio so users who are deaf or hard of hearing can follow along. It also means audio descriptions for video content where visual information is important and not captured in the dialogue, so that users who are blind or have low vision can understand what is happening on screen.

The third area is Adaptable Content. Content should be structured so it can be presented in different ways without losing meaning. In practice this means using proper HTML semantics. If something is a heading, mark it up as a heading element. If something is a list, use a list element. Don't just make text look like a heading by making it large and bold. Use the actual heading tag. Assistive technologies rely on this semantic structure to present content in alternative ways, like reading out a document outline or navigating between sections.

The fourth area is Distinguishable. Content needs to be easy to see and hear. This covers things like colour contrast, where the text on your page needs sufficient contrast against its background for users with low vision or colour vision deficiencies to read it. It also means you shouldn't rely on colour alone to convey information. If you're showing an error message in red, include an icon or text label as well, because not all users will perceive the colour. Additionally, text should be resizable without breaking the layout of the page.

---

## Slide 10: Operable

**Slide content:** *Users must be able to interact with and navigate the interface.* Interfaces must support alternatives to mouse control. Five areas: Keyboard Accessible, Enough Time, Seizures and Physical Reactions, Navigable, Input Modalities.

**Script:**

The second principle is Operable. This means users must be able to interact with and navigate your interface. Critically, this includes users who are not using a mouse. Many people who use assistive technology navigate entirely by keyboard, or by switch devices that emulate keyboard input. If your interface requires a mouse to use, you've locked those users out.

WCAG breaks operability into five areas.

The first area is keyboard accessibility. Everything that can be done with a mouse must also be doable with a keyboard alone — clicking buttons, filling out forms, opening and closing menus and dialogs, all of it. This also includes ensuring keyboard focus is always visible, so users navigating by keyboard can see where they are on the page at any given time.

The second is giving users enough time. If your content or interface has a time limit, like a session timeout or an auto-advancing carousel, users must be given enough time to read and interact with it, or be able to pause, stop, or extend it. Someone using a screen reader or switch device may simply take longer to navigate through content, and time limits that work fine for a mouse user can be a significant barrier.

Third is avoiding seizure and physical reaction triggers. Content that flashes or strobes rapidly can trigger seizures in users with photosensitive epilepsy. WCAG's rule is that nothing on the page should flash more than three times per second. This might seem like an edge case, but the consequences of getting it wrong are serious.

Fourth is making your interface navigable. Users need to be able to move through your page efficiently and find what they're looking for. This covers things like having descriptive page titles, using link text that makes sense out of context — so instead of 'click here' you say what the link actually goes to — and ensuring a logical tab order when moving through interactive elements. It also covers skip navigation links, which let keyboard users jump past repeated navigation and go straight to the main content.

Finally, input modalities. Not everyone interacts with a screen the same way, so functionality shouldn't rely solely on complex gestures or precise pointer movements. Think about a map with pinch-to-zoom — that gesture might not be available to all users, so you'd also want to provide buttons to zoom in and out. More broadly, touch targets should be large enough to be easily activated, and functionality should work across a variety of input methods.

---

## Slide 11: Understandable

**Slide content:** *Both the content and the interface behaviour must be clear and predictable.* Three areas: Readable, Predictable, Input Assistance.

**Script:**

The third principle is Understandable. This means that not only does content need to be perceivable and the interface operable, it all needs to be clear and predictable. Even if a user can technically access your content, if the interface behaves unexpectedly or the content is confusing, the experience breaks down.

WCAG defines three areas here.

The first area is readability. Text content needs to be readable and understandable, and one concrete example of this is identifying the language of your page in HTML using the lang attribute. This might seem like a small detail, but it matters a lot for screen readers — a screen reader needs to know what language a page is in so it can pronounce words correctly. If your page has sections in a different language from the rest, those should be marked with a lang attribute on the relevant elements as well.

The second is predictability. Pages should behave in expected ways — your navigation should look consistent across pages, and things shouldn't change unexpectedly without the user initiating it. For example, changing the page or submitting a form when a user selects a dropdown item, without them pressing a button, can be very disorienting, especially for screen reader users.

The third area is input assistance. When users fill out forms, errors should be described clearly and helpfully. Instead of a generic popup that just says 'Error,' tell the user specifically what went wrong and how to fix it. Instead of just flagging a postal code field as invalid, say 'Please enter your postal code in the format A1A 1A1.' The more specific and actionable the feedback, the better — and honestly this is just good UX practice for everyone, not just users with disabilities.

---

## Slide 12: Robust

**Slide content:** *Content must be built with correct, modern code so it works reliably with browsers and assistive technologies.* Use semantic HTML — e.g., `<button>` instead of a `<div>` with a click handler. Resource: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility

**Script:**

The fourth and final principle is Robust. This one is aimed squarely at developers. It means your web content should be built using correct, current code so that it can be reliably interpreted by browsers and assistive technologies.

The core idea is to use the right tool for the job. HTML has a rich set of semantic elements, elements that carry meaning about the role they play in a document or interface. When you use semantic elements correctly, browsers and assistive technologies can interpret your interface accurately and respond to it the way that users expect.

Here is a classic example. You can make something look and behave like a button using a div element with some CSS and a JavaScript click handler. It might look identical to a real button on screen. But a screen reader looking at a div has no idea that element is interactive. It will not announce it as a button, it will not be focusable by keyboard by default, and a user navigating without a mouse might never find it. If you use an actual button element, all of that comes for free. The browser already knows it's a button, screen readers already know how to handle it, and keyboard navigation already works.

So the principle is: wherever a native HTML element exists for what you are trying to build, use it. This applies to buttons, headings, links, lists, form fields, navigation regions, and more. If you're ever unsure whether a specific element exists for what you're building, MDN Web Docs is an excellent resource. Their accessibility documentation in particular is very thorough. You can find that and all other links I mention on the resource page. I'll include the link to the resource page at the end of this video.

---

## Slide 13 — ARIA: The Problem

**Slide content:** Code — plain div with no ARIA. Visual render — progress bar at 75%. Screen reader output — "75%"

**Script:**

Before we move on from the technical side of WCAG, there's one more tool worth knowing about: ARIA, which stands for Accessible Rich Internet Applications. To understand why ARIA exists, let's look at a concrete example.

Here we have a progress bar built using a plain div. To a sighted user it looks completely fine — there's a bar, and it shows 75%, the visual is clear. But look at what a screen reader gets from this: just '75%'. No context. Is that a percentage, if so of what? A label? A score? The screen reader has no idea that it's looking at a progress bar because a div carries no semantic meaning on its own. It's just a box.

source for ARIA: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/WAI-ARIA_basics

---

## Slide 14 — ARIA: The Solution

**Slide content:** Code — div with role="progressbar", aria-valuenow, aria-valuemin, aria-valuemax. Visual render — identical progress bar. Screen reader output — "Progress bar, 75 percent. Minimum 0, maximum 100." First rule of ARIA: use native HTML first. MDN link on resource website.

**Script:**

This is where ARIA comes in. By adding role='progressbar' and the aria-value attributes to the same div, we've given the screen reader everything it needs. Now instead of '75%' it announces 'Progress bar, 75 percent. Minimum 0, maximum 100.' Same visual, completely different experience for a screen reader user.

There's a well-known principle called the first rule of ARIA: if a native HTML element already exists with the semantics you need, use that instead. A native button, a native input, a native nav — these all come with built-in accessibility information for free. ARIA is for situations like this one, where no native element exists for what you're building.

It's also worth knowing that bad ARIA is worse than no ARIA. Applied incorrectly, ARIA attributes can actively mislead assistive technologies and make an interface harder to use than if nothing had been added at all. So use native HTML first, and reach for ARIA carefully and deliberately when you actually need it. I'll link the MDN documentation on the resource website if you want to dig deeper.

---

## Slide 15: What Does EN 301 549 Add Beyond WCAG?

**Slide content:** EN 301 549 covers non-web systems: operating systems, native applications, closed systems (e.g., kiosks), and authoring tools (e.g., VS Code, Microsoft Word). Mention of ATAG 2.0.

**Script:**

Ok, so we've covered WCAG in detail. Now let's look at what EN 301 549 adds beyond that.

WCAG is focused specifically on web content, while EN 301 549 takes a much broader view. It defines accessibility requirements for all kinds of software and technology, including operating systems, native desktop and mobile applications, software running on closed systems like kiosks or ATMs, and authoring tools.

That last category, authoring tools, is an interesting one. Authoring tools are applications used to create content, things like VS Code, Microsoft Word, or Adobe products. EN 301 549 addresses not just whether these tools are accessible to use, but also whether the content they generate is accessible. The idea is that if you are building a tool other people use to create content, your tool should make it easy, or ideally the default, to produce accessible output. The specifics of this are defined in a separate standard called ATAG 2.0, the Authoring Tools Accessibility Guidelines. We're not going to go deep on ATAG in this video, but if you are ever building something that would be considered an authoring tool, that is the standard to look at.

The other major thing EN 301 549 adds is a detailed framework for how software systems should interact with assistive technology. It defines how an accessibility API needs to expose information, things like the role of an interface element, its current state, and its name and description, so that assistive technologies like screen readers and braille displays can read and interact with the interface. It also defines obligations on the assistive technology side, covering how AT needs to interact with the APIs that systems expose. This bidirectional definition is what makes the whole ecosystem work. Without it, there would be no guarantee that a screen reader built by one company could interact with an operating system built by another.

---

## Slide 16: Tools to Help You Build Accessibly

**Slide content:** Three tools: (1) Contrast Checker — WebAIM: webaim.org/resources/contrastchecker, (2) Color Filter — simulates colour vision deficiency, (3) Automated checking tool — e.g., Google Lighthouse.

**Script:**

Now that we understand the standards, let's talk about some practical tools that can help you check whether what you are building is actually accessible.

The first is a contrast checker. These tools let you input two colours, a foreground and a background, and check whether the contrast ratio between them meets WCAG requirements. The standard sets minimum contrast ratios for text, with higher requirements for smaller text. The one I'd recommend starting with is WebAIM's contrast checker, which is also linked on the resource page. It's free, straightforward to use, and tells you exactly which WCAG conformance levels your contrast ratio passes or fails. Many design tools like Figma also have contrast checking built in, but the WebAIM tool is a reliable fallback for checking any combination of colours.

The second type of tool is a colour filter or colour blindness simulator. These let you view your interface as it would appear to someone with a colour vision deficiency. There are different types of colour blindness, and a good simulator will let you check several of them. This is useful for catching situations where you are accidentally relying on colour alone to convey information, which the Distinguishable criterion under Perceivable specifically flags as a problem.

The third, and probably the most powerful for a developer, is an automated accessibility checking tool. Google Lighthouse is a great example. It is built right into Chrome's developer tools, and it can audit a live web page for a range of accessibility issues, give you a score, and provide specific recommendations. It is not a complete solution since automated tools can only catch a subset of accessibility issues and there are things that require human judgment. But it is an excellent starting point and a great way to catch obvious issues quickly.

Let's take a look at Lighthouse in action.

webaim.org/resources/contrastchecker
---

## Slide N/A: Demo — Google Lighthouse

**Slide content:** Demo slide — minimal text, perhaps a screenshot placeholder or the URL of the demo page.

**Script:**

I've spun up a simple web page for this demo. Let me walk you through how to use Lighthouse to audit it.

[Run your demo here. Open Chrome DevTools, navigate to the Lighthouse tab, run the audit, and walk through the results. Narrate what you are clicking and what each section of the report means as you go. Point out specific issues it flags and explain what they mean in terms of the WCAG criteria we covered.]

A few things to keep in mind as you look at these results: Lighthouse gives you a score out of 100, but that score is not the whole story. It's testing for things it can automatically detect, like missing alt text, insufficient colour contrast, and missing form labels. There are entire categories of accessibility issues that automated tools can't catch. Things like whether content is logically structured, whether error messages are actually helpful, or whether the overall experience makes sense for someone using a screen reader. That's why automated testing is a starting point, not a finishing line.

---

## Slide 17: Beyond Tools — Inclusive Development Practices

**Slide content:** The gold standard: include users with accessibility needs in your development process, ideally from requirements and specifications onward. Alternative: cognitive walkthroughs using user personas.

**Script:**

Alright, tools are helpful, but let's talk about what best practice actually looks like when it comes to building accessible software.

The gold standard, and this is widely agreed upon in the accessibility community, is to involve users who have accessibility needs directly in your development process. This means more than just testing with them at the end. Ideally you are including these users during requirements gathering and specifications, so that accessibility needs are informing design decisions from the very beginning rather than being retrofitted later.

The reason lived experience matters so much here is that it's difficult for a developer to anticipate every way a user might interact with a system. A tester who uses a screen reader every day will notice things that a developer who's never used one would simply miss. They'll notice when the focus order is confusing, when an error message is unhelpful in a specific way, or when a feature works technically but is still frustrating to use in practice. That kind of feedback is invaluable and very hard to replicate through developer testing alone.

If you don't have access to testers who use assistive technology or adaptive hardware, and often in academic or small team contexts you won't, a structured alternative is to conduct a cognitive walkthrough using user personas. This is a technique covered in CSCI 310, Human Computer Interaction. You create detailed personas representing users with different accessibility needs and walk through your software's key tasks from their perspective, asking at each step whether this persona would be able to complete this task and what barriers they might encounter. It's not as effective as real user testing, but it is a structured and methodical way to catch issues you might otherwise miss.

---

## Slide 18: Summary and Wrap-Up

**Slide content:** Key takeaways. 

**Script:**

Let's wrap up with some key takeaways.

Accessibility is about ensuring your software is equally available to users with disabilities or other barriers to use. It needs to be built in from the start, not just added at the end.

The two main standards are WCAG and EN 301 549 V3. WCAG is your primary reference for web development, organized around the four POUR principles: Perceivable, Operable, Understandable, and Robust. EN 301 549 incorporates WCAG and extends it to cover native applications, operating systems, kiosks, and authoring tools, and defines how systems must interact with assistive technology. In Canada, EN 301 549 V3 has been legislated federally through the Accessible Canada Act.

Practical tools like contrast checkers, colour filters, and Lighthouse can help you catch issues, but they're not a substitute for thoughtful, inclusive development practice. When native HTML elements aren't enough, ARIA provides a way to give assistive technologies the information they need, though it should always be a last resort after native semantics. The gold standard is involving users with accessibility needs directly in your process from the beginning.

Yes, accessibility adds development cost — but building it in from the start costs significantly less than retrofitting it later, it widens your potential user base, and it gets easier the more you do it. It's one of those areas where doing the right thing and doing the practical thing happen to point in the same direction.

---

## Slide 19: Thanks and Bye

**Slide content:** Thank you, Link to course resource website.

**Script:**

For all the links I mentioned and more, check out the resource website at the link on the screen. I've included the WCAG quick reference guide, the MDN accessibility docs, and several other tools and references there. 

Thank you for watching.