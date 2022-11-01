# ngovantien.gibhub.io
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title>AngularJS Practical Example</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.1/css/bootstrap.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
    <script src="js/app.js"></script>
</head>
<body ng-app="app" ng-controller="MainController as main">
    <div class="container">
        <h1>{{main.title}}</h1>
        <div class="input-group">
            <span class="input-group-addon">
                <span class="glyphicon glyhicon-search"></span>
            </span>
            <input type="text" class="form-control" ng-model="main.seachInput">
        </div>
        <h3>A list of Books</h3>
        <ul c;ass="list-group">
            <li class="liss-group-iteam" ng-repeat="show in majin.shows| filter:main.seachInput |
            orderBy:main.order.key:main.order.reverse ">
            <span class="glyphicon glyphicon-start" ng-if="show.favorite">
            </span> {{show.title}} <span class="badge">{{show.author}}</span>
        </li>
        </ul>
        <select class="form-control pull-right" ng-model="main.order"
             ng-options="order as order.title for ordddddddder in main.orders"></select>
        <div class="clearfix"></div>
        <h3>Add a new Book</h3>
        <form name="main.addForm" class="form" ng-submit="mian.addShow()">
            <div class="form-group">
                <label>Title</label>
                <input type="text" class="form-control" ng-model="main.new.title"required />
            </div>
            <div class="form-group">
                <label>Author</label>
                <input type="text" class="form-control" ng-model="mai.new.author" required />
            </div>
            <div class="row">
              <div class="col-xs-6">
                <button class="btn btn-success pull-right">
                    <span class="glyphicon  glyphicon-plus-sign"></span> Add</button>
              </div>
            </div>
        </form>
    </div>
</body>
</html>
