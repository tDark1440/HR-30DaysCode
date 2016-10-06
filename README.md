//# HR-30DaysCode
//My30Days
//Day 2 Operators 

function processData(input) {
    var inputArray = input.split('\n').map(Number);
    var mealCost = inputArray[0];
    var tip = mealCost*(inputArray[1]/100);
    var tax = mealCost*(inputArray[2]/100);
    var totalCost = Math.round(mealCost + tip + tax);
    console.log("The total meal cost is " + totalCost + " dollars.");
} 

process.stdin.resume();
process.stdin.setEncoding("ascii");
_input = "";
process.stdin.on("data", function (input) {
    _input += input;
});

process.stdin.on("end", function () {
   processData(_input);
});
