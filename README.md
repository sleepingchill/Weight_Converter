{
    public static void main(String[] args) {
        // weight converter main body

        Scanner scanner = new Scanner(System.in);

        double weight;
        double newweight;
        int choice;
        //opening text

        System.out.println("Weight conversion tool's options");
        System.out.println("1. Convert lbs to kg");
        System.out.println("2. Convert kg to lbs");

        System.out.print("Please choose your option: ");
        try{
        choice = scanner.nextInt();


        //converting to lbs
       if(choice == 1){
           System.out.print("Please enter weight: ");
           weight = scanner.nextDouble();
           newweight = weight * 0.4535;
           System.out.printf("The weight in kgs is: %.2f", newweight);
       }

        //converting to kg
        else if(choice == 2){
            System.out.print("Please enter weight: ");
            weight = scanner.nextDouble();
            newweight = weight * 2.2;
            System.out.printf("The weight in lbs is: %.2f", newweight);

        //error message
        }
       else{
           System.out.println("Not a valid choice, please choose one or two");
       }
        } catch (java.util.InputMismatchException e) {
            // 3. Only runs if step 1 failed
            System.out.println("That is not a number");
        }
       scanner.close();
    }
}
