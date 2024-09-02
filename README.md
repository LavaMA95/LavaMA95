void main() {
  
  List<User> users = [
    User(name: 'Ahmed', age: 25, gender: 'Male'),
    User(name: 'Sara', age: 22, gender: 'Female'),
    User(name: 'Ali', age: 30, gender: 'Male'),
    User(name: 'Mona', age: 28, gender: 'Female'),
    User(name: 'Hassan', age: 35, gender: 'Male'),
    User(name: 'Laila', age: 27, gender: 'Female'),
    User(name: 'Omar', age: 24, gender: 'Male'),
    User(name: 'Nour', age: 26, gender: 'Female'),
    User(name: 'Khaled', age: 29, gender: 'Male'),
    User(name: 'Dina', age: 23, gender: 'Female'),
  ];
  List<User> getMaleUsers(List<User> users) {
    return users.where((user) => user.gender == 'Male').toList();
  }   
  List<User> getFemaleUsers(List<User> users) {
    return users.where((user) => user.gender == 'Female').toList();
  }       
  List<User> maleUsers = getMaleUsers(users);
  print('Male Users:');
  maleUsers.forEach((user) => print(user.name));
  print('Total Male Users: ${maleUsers.length}');       
  List<User> femaleUsers = getFemaleUsers(users);
  print('Female Users:');
  femaleUsers.forEach((user) => print(user.name));
  print('Total Female Users: ${femaleUsers.length}');
}
class User {
  String name;
  int age;
  String gender;
  User({required this.name, required this.age, required this.gender});
}
