
      /**
       *
       *                 Board                               Display
       *                 ------                               ------
       *    (EN2)  PB5  | 1  2 | PA15(BTN_ENC)            5V |10  9 | GND
       *  (LCD_CS) PA9  | 3  4 | RST (RESET)              -- | 8  7 | --
       *  (LCD_A0) PA10   5  6 | PB9 (EN1)            (DIN)  | 6  5   (RESET)
       *  (LCD_SCK)PB8  | 7  8 | PD6 (MOSI)         (LCD_A0) | 4  3 | (LCD_CS)
       *            GND | 9 10 | 5V                (BTN_ENC) | 2  1 | --
       *                 ------                               ------
       *                  EXP1                                 EXP1
       *
       *                                                      ------
       *                                                  -- |10  9 | --
       *                   ---                       (RESET) | 8  7 | --
       *                  | 3 |                      (MOSI)  | 6  5   (EN2)
       *                  | 2 | (DIN)                     -- | 4  3 | (EN1)
       *                  | 1 |                     (LCD_SCK)| 2  1 | --
       *                   ---                                ------
       *                Neopixel                               EXP2
       *
       * Needs custom cable. Connect EN2-EN2, LCD_CS-LCD_CS and so on.
       *
       * Check the index/notch position twice!!!
       * On BTT boards pins from IDC10 connector are numbered in unusual order.
       */
      #define BTN_ENC                EXP1_02_PIN
      #define BTN_EN1                EXP1_06_PIN
      #define BTN_EN2                EXP1_01_PIN
      #define BEEPER_PIN                    -1

      #define DOGLCD_CS              EXP1_03_PIN
      #define DOGLCD_A0              EXP1_05_PIN
      #define DOGLCD_SCK             EXP1_07_PIN
      #define DOGLCD_MOSI            EXP1_08_PIN

      #define FORCE_SOFT_SPI
      #define LCD_BACKLIGHT_PIN             -1
