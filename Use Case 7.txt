public class OOPSBANNERAPP3 {

    static class CharacterPattern {

        private char letter;
        private String[] pattern;

        public CharacterPattern(char letter, String[] pattern) {
            this.letter = letter;
            this.pattern = pattern;
        }

        public String[] getPattern() {
            return pattern;
        }
    }

    public static void main(String[] args) {

        CharacterPattern O1 = new CharacterPattern('O', new String[]{
                " ***** ",
                "*     *",
                "*     *",
                "*     *",
                " ***** "
        });

      
        CharacterPattern O2 = new CharacterPattern('O', new String[]{
                " ***** ",
                "*     *",
                "*     *",
                "*     *",
                " ***** "
        });

        
        CharacterPattern P = new CharacterPattern('P', new String[]{
                " ***** ",
                "*     *",
                " ***** ",
                "*      ",
                "*      "
        });

      
        CharacterPattern S = new CharacterPattern('S', new String[]{
                " ***** ",
                "*      ",
                " ***** ",
                "      *",
                " ***** "
        });

      
        CharacterPattern[] word = {O1, O2, P, S};

        int height = 5;

        for (int row = 0; row < height; row++) {

            StringBuilder line = new StringBuilder();

            for (CharacterPattern cp : word) {
                line.append(cp.getPattern()[row]).append("   ");
            }

            System.out.println(line);
        }
    }
}