- 👋 Hi, I’m @JasonSon5357
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
JasonSon5357/JasonSon5357 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Pl don't swear
Here's a blooket hack...
for add tokens.
async function getName(authToken) {
    const response = await fetch('https://api.blooket.com/api/users/verify-token?token=JWT+' + authToken);
    const data = await response.json();

    return data.name
};

async function addTokens() {
    const add_tokens = prompt('How many tokens do you want to add to your account? (500 daily)');
    const myToken = localStorage.token.split('JWT ')[1];

    if (add_tokens > 500) {
        alert('You can add up to 500 tokens daily')
    }

    const response = await fetch('https://api.blooket.com/api/users/add-rewards', {
        method: "PUT",
        headers: {
            "referer": "https://www.blooket.com/",
            "content-type": "application/json",
            "authorization": localStorage.token
        },
        body: JSON.stringify({
            name: await getName(myToken),
            addedTokens: add_tokens,
            addedXp: 300
        })
    });

    if (response.status == 200) {
        alert(`${add_tokens} added to your account!`);
    } else {
        alert('An error occured.');
    };

};

addTokens();











the end,,, thanks to blooket hack improved glixzzy that I could get this hack.
$sudo hack everybody $100000000

