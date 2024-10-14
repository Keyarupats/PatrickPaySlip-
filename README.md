public class Main {
	public static void main(String[] args) {

		int a = 10;
		int b = 20;
		int c = 30;
		int d = 40;
		int e = 50;
        a += 5;
        a /= 5;

		int add = a + b;
		int diff = d - c;
		int kagibunshin = e * a;

		System.out.println("ADDITION: " + add);
		System.out.println("SUBTRACTION: " + diff);
		System.out.println("MULTIPLICATION: " + kagibunshin);
		System.out.println();
		System.out.println("AND: " + (a < c && b > d));
		System.out.println("OR: " + (a < b || e < d));
		System.out.println();

		if (e != b) {
			System.out.println(" Eguls Mossing! ");
		} else {
			System.out.println("SSAP MOSSING! ");
		}

		System.out.println();
		for (int kupal = 1; kupal <= 10; kupal++) {
			System.out.println("WALA LANG MOSSING! " + kupal);
			System.out.println(" ");

		}


	}
}
