## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `11:59 PM - 27/04/2024`
* The branch name for your repo should be: `assignment`
* What to submit for this assignment:
    * This markdown file (assignment.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/shell/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

# Assignment: The Secret Password

You are stuck in a virtual room and can only leave if you figure out the password! Fortunately, somebody left behind 6 clues for you to find the secret password, but the messaging is not that clear. It is your job to discover what the secret password is!

1. The very odd and inedible ingredient in a cake recipe
2. The season number that contains only 18 episodes (Hint: How do you list them?)
3. Fifth word of Season 6, Episode 21 of Friends
4. Fifth word of the fifth fictional Space Wars series
5. Second word of this song that's exactly 4 minutes long in this "colour" album
6. The fourth word to the fourth Hunger Games movie

## Instructions
1. Fork this Shell learning module repository following these [instructions](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#setting-up)
2. Use your bash skills (such as `cd`, `cat`, etc.) to figure out what the secret password is! You will be exploring the `clues` directory in your bash terminal.
3. Write the secret password in your own version of this markdown file in your forked repo.

**What is the secret password?**
```
Your answer here...
1.So I am at assignment folder now
cd ..
"cd cluse"-> "ls" get recipe list
Then cat contents of the three txt, then find out "paper ring" is the odd one.

2.cd ../../ then cd shows ls
to find the count of item in each folder use this command: find . -mindepth 1 -maxdepth 1 -type d -exec sh -c 'printf "%s:\t" "$1"; ls -A "$1" | wc -l' _ {} \; | sort -k 2 -n
and you get this:
./season_10:          18
./season_1:           24
./season_2:           24
./season_4:           24
./season_5:           24
./season_7:           24
./season_8:           24
./season_9:           24
./season_3:           25
./season_6:           25

so the second answer is "10"

3.cd season_6 cat ep_21.txt. you get "The One Where Ross Meets Elizabeth's Dad" fifth word is "meets"

4.cd space_wars/fifth_movie.txt you get "Space Wars: Future Legends and Past Legacies" so the answer here is "Legacies"

5.find albums -type f -name "*.txt" -exec cat {} \;

Title: Red
Duration: 3:43
Title: Everything Has Changed
Duration: 4:05
Title: I Knew You Were Trouble
Duration: 3:39
Title: The Lucky One
Duration: 4:00
Title: Holy Ground
Duration: 3:22

This prints all the content of text file under album folder. so the answer for this one is "Lucky".

6.cd ../../ cd movies/hanger_games cat movie4.txt
the answer for this one is "stars"

In conclusion, based on the 6 clues, the secure key is "Paper ring 10 meets Legacies Lucky stars"





```

|Criteria|Complete|Incomplete|
|---|---|---|
|Secret Password|The user properly used the proper bash commands to find the secret password.|The user did not properly used the proper bash commands to find the secret password.|



If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-3-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
