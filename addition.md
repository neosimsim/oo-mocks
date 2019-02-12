# Functional

	1 + 2

or

	add 1 2


# OO

	addition = new Addition()
	addition.setSummand1(1)
	addition.setSummand2(2)
	addition.add()
	addition.getResult()

or do it like a pro:

	public abstract class Addition {
		private int result;

		public void execute() {
			result = getSummand1() + getSummand2();
		}

		public int getResult() {
			return result;
		}

		protected abstract getSummand1();
		protected abstract getSummand2();
	}

	public class Add3And4 extends Addition {

		protected getSummand1() {
			return 3;
		}

		protected getSummand1() {
			return 4;
		}
	}

and then call

	addition = new Add3And4();
	addition.execute();
	result = addition.result();
