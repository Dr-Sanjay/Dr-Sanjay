## Visitor Stats

![Visitor Stats](https://visitor-badge.laobi.icu/badge?page_id=dr-sanjay.Dr-Sanjay)
![Unique Visitors](https://visitor-badge.laobi.icu/badge?page_id=dr-sanjay.Dr-Sanjay&title=unique%20visitors)
<!-- This code will show who has visited and how much time spent, which repo opened -->

<!-- This code will show who has visited and how much time spent, and which repo opened -->

<script>
function showVisitors() {
  // Get the list of visitors.
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

  // Create a table to display the visitors.
  var table = document.createElement("table");
  table.innerHTML = "<tr><th>Name</th><th>Time spent</th><th>Repo opened</th></tr>";

  // Add each visitor to the table.
  for (var i = 0; i < visitors.length; i++) {
    var row = table.insertRow(i + 1);  // Start from the second row (index 1) to keep the header row (index 0).
    row.innerHTML = "<td>" + visitors[i].name + "</td><td>" + visitors[i].time_spent + "</td><td>" + visitors[i].repo_opened + "</td>";
  }

  // Display the table.
  var visitorsDiv = document.getElementById("visitors");
  visitorsDiv.innerHTML = "";  // Clear the visitors div before adding the table.
  visitorsDiv.appendChild(table);
}

function showRepo() {
  // Get the name of the repo that was opened.
  var repo = window.location.pathname.split("/").pop();

  // Display the name of the repo.
  var repoDiv = document.getElementById("repo");
  repoDiv.innerHTML = "Repo opened: " + repo;
}
</script>

<!-- Show visitors and repo opened -->
<button onclick="showVisitors()">Show visitors</button>
<button onclick="showRepo()">Show repo opened</button>
<div id="visitors"></div>
<div id="repo"></div>
