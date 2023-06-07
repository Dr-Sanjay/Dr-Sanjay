## Visitor Stats

![Visitor Stats](https://visitor-badge.laobi.icu/badge?page_id=dr-sanjay.Dr-Sanjay)
![Unique Visitors](https://visitor-badge.laobi.icu/badge?page_id=dr-sanjay.Dr-Sanjay&title=unique%20visitors)
<!-- This code will show who has visited and how much time spent, which repo opened -->

<script>
function showVisitors() {
  var visitors = [
    {
      "name": "John Doe",
      "time_spent": 1000,
      "repo_opened": "my-repo"
    },
    {
      "name": "Jane Doe",
      "time_spent": 500,
      "repo_opened": "your-repo"
    }
  ];

  var table = document.createElement("table");
  table.innerHTML = "NameTime spentRepo opened";

  for (var i = 0; i < visitors.length; i++) {
    var row = table.insertRow(i + 1);
    row.innerHTML = "<td>" + visitors[i].name + "</td><td>" + visitors[i].time_spent + "</td><td>" + visitors[i].repo_opened + "</td>";
  }

  var visitorsDiv = document.getElementById("visitors");
  visitorsDiv.innerHTML = "";
  visitorsDiv.appendChild(table);
}

function showRepo() {
  var repo = window.location.pathname.split("/").pop();
  var repoDiv = document.getElementById("repo");
  repoDiv.innerHTML = "Repo opened: " + repo;
}
</script>

Show visitors <button onclick="showVisitors()">Show visitors</button>
Show repo opened <button onclick="showRepo()">Show repo opened</button>
<div id="visitors"></div>
<div id="repo"></div>
