<!DOCTYPE html>
<html>
<body>
    <h1>Countdown Timer</h1>
    <h2>Countdown from 20 seconds to 0 seconds</h2>

    <button type = button onclick = "startCountdown()">Start Countdown</button>

    <h3 id="demo"></h3>

    <script>
    let timer;

    function startCountdown() {
        clearInterval(timer);
        let count =20;
        myDisplayer(count);

        timer = setInterval(function() {
            count--;
            myDisplayer(count);

            if (count === 0) {
                clearInterval(timer);
                myDisplayer("Countdown finished");
            }
        },1000);

    }
    //function myDisplayer(text){
        //let demo = document.getElementById("demo");
        //demo.innerHTML = text;
    //}
    function myDisplayer(count){
        document.getElementById("demo").innerHTML = count;
    }
    </script>

</body>
</html># Simple-countdown
Countdown from 20 to 0 second
