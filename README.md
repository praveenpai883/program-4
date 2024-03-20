<!DOCTYPE html>
<html>
<head>
<title>AngularJS Factorial and Square Calculator App</title>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"> 
</script>
</head>
<body>
 <div ng-app="myApp" ng-controller="myCtrl">
<h1>Factorial and Square Calculator App</h1>
<input type="number" ng-model="number" placeholder="Enter a Number">
<button ng-click="calculateFactorial()">Calculate Factorial</button>
<button ng-click="calculateSquare()">Calculate Square</button>
<p>Factorial: {{factorial}}</p>
<p>Square: {{square}}</p>
 </div>
<script>
var app = angular.module("myApp", []);
app.controller("myCtrl", function($scope) {
 $scope.number = 0;
 $scope.factorial = 0;
 $scope.square = 0;
$scope.calculateFactorial = function() {
 var factorial = 1;
 for (var i = $scope.number; i > 1; i--) {
 factorial *= i;
 }
 $scope.factorial = factorial;
};
 $scope.calculateSquare = function() {
 $scope.square = $scope.number * $scope.number;
};
});
</script>
</body>
</html>
