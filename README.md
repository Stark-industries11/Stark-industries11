- 👋 Hi, I’m @Stark-industries11
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Stark-industries11/Stark-industries11 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

#include <stdio.h>

int main() {
    int budget;
    int potatoPrice = 30;
    int tomatoPrice = 50;
    int bananaPrice = 10;

    int maxPotatoQty = 2;
    int maxTomatoQty = 3;
    int maxBananaQty = 5;

    int potatoQty = 0;
    int tomatoQty = 0;
    int bananaQty = 0;

    printf("Enter your budget: ");
    scanf("%d", &budget);

    if (budget >= 0) {
        potatoQty = budget / potatoPrice;
        if (potatoQty > maxPotatoQty) {
            potatoQty = maxPotatoQty;
        }
        budget -= potatoQty * potatoPrice;

        tomatoQty = budget / tomatoPrice;
        if (tomatoQty > maxTomatoQty) {
            tomatoQty = maxTomatoQty;
        }
        budget -= tomatoQty * tomatoPrice;

        bananaQty = budget / bananaPrice;
        if (bananaQty > maxBananaQty) {
            bananaQty = maxBananaQty;
        }
        budget -= bananaQty * bananaPrice;

        printf("You got %d kg of potato.\n", potatoQty);
        printf("You got %d kg of tomato.\n", tomatoQty);
        printf("You got %d banana.\n", bananaQty);

        if (budget > 0) {
            printf("Remaining balance: Rs %d\n", budget);
        } else {
            printf("Balance over.\n");
        }
    } else {
        printf("Invalid budget.\n");
    }

    return 0;
}
