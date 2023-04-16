```html

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>LeetCode Stats</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.4.1/semantic.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.4.1/semantic.min.js"></script>
</head>
<body>
    <div class="ui container">
        <h1 class="ui header">LeetCode Stats</h1>
        <div class="ui segment">
            <div class="ui four statistics">
                <div class="statistic">
                    <div class="value" id="totalSolved"></div>
                    <div class="label">Total Solved</div>
                </div>
                <div class="statistic">
                    <div class="value" id="easySolved"></div>
                    <div class="label">Easy Solved</div>
                </div>
                <div class="statistic">
                    <div class="value" id="mediumSolved"></div>
                    <div class="label">Medium Solved</div>
                </div>
                <div class="statistic">
                    <div class="value" id="hardSolved"></div>
                    <div class="label">Hard Solved</div>
                </div>
            </div>
        </div>
    </div>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
        $(document).ready(function() {
            $.getJSON("leetcode-stats.json", function(data) {
                $("#totalSolved").text(data.totalSolved);
                $("#easySolved").text(data.easySolved);
                $("#mediumSolved").text(data.mediumSolved);
                $("#hardSolved").text(data.hardSolved);
            });
        });
    </script>
</body>
</html>

```
