Goal:
The main goal of this project was to create a simple yet secure login page as part of a Capture The Flag (CTF) style challenge. The challenge is designed to test participants’ ability to analyze web applications and discover hidden credentials by exploring Git history and code changes.

Description:
I developed a login page using HTML, CSS, and JavaScript, with the username and password validation hardcoded into a JavaScript function. The password is intentionally made complex to encourage careful inspection of the source code and Git commits.

To make the challenge more interesting, the original login logic was added in an early commit and later removed or obfuscated, requiring users to explore Git history to retrieve the credentials.

This project demonstrates practical skills in:

Web development basics (HTML/CSS/JS)

Version control analysis using Git

Reverse engineering and code auditing

Code Excerpt:

<script>
  function login() {
    let form = document.getElementById("login-form");
    let username = form.elements["username"].value;
    let password = form.elements["password"].value;
    if (
      username === "admin" &&
      password === "Th1s_1s_4_L0ng_4nd_S3cur3_P4ssw0rd!"
    ) {
      document.cookie = "login=1";
      window.location.href = "/dashboard.html";
    } else {
      document.getElementById("error").innerHTML =
        "INVALID USERNAME OR PASSWORD!";
    }
  }
</script>
Conclusion:
I built this project to sharpen my understanding of how web authentication can be implemented and how sensitive information might accidentally be exposed through version control. It also serves as an educational tool for those learning to audit code and extract valuable insights from Git repositories.
