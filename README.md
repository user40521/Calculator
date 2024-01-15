������ 1: �����������
��������
�������� ����� Calculator. � ��� �������� ����������� ���������� ���� Supplier. ��� �������������� ���������, ����������� ����� get(). � ������� ������ ���������� ����� ����� �������� ��������� ������ Calculator. ���������� ������ �� ����� ������������ ������ Calculator() { }.

static Supplier<Calculator> instance = Calculator::new;
����� �������� ��������� ���������� ���� BinaryOperator ��� �������������� �������� ��� ����� �������. ����������� �� ��� Integer:

BinaryOperator<Integer> plus = (x, y) -> x + y;
BinaryOperator<Integer> minus = (x, y) -> x - y;
BinaryOperator<Integer> multiply = (x, y) -> x * y;
BinaryOperator<Integer> devide = (x, y) -> x / y;
�������� ��������� ���������� ���� UnaryOperator ��� ������������ �������������� �������� ��� ����� ������:

UnaryOperator<Integer> pow = x -> x * x;
UnaryOperator<Integer> abs = x -> x > 0 ? x : x * -1;
�������� ���������� ���� Predicate ��� ����������� ������������� �� �����:

Predicate<Integer> isPositive = x -> x > 0;
�������� ���������� ���� Consumer ��� ������ ����� � �������. ����������� ��� ����� ������ �� ����������� ����� println():

Consumer<Integer> println = System.out::println;
����������
� ������ Main � ������ main() �������� ��������� ������ Calculator ����� ����� ����������� ���������� instance:

Calculator calc = Calculator.instance.get();
����������� ��������� �������������� �������� ��� �������:

int a = calc.plus.apply(1, 2);
int b = calc.minus.apply(1,1);
int c = calc.devide.apply(a, b);
� �������� � ������� ���������:

calc.println.accept(c);
�������� �������� �� ��, ��� ����������� ���� ��� �������� �� �����. � ������� ����������� � ���� ��������� ������� ������������� ������, � ��� ����������� ������ � ������� �� �������. �������� ����������, � ������� ������������� ��������� ����������� ������.