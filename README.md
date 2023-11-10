# dz-with-Kata
import random
def guess_the_number():
    secret_number = random.randint(1, 100)
    attempts = 0
    guessed = False
    print("Вгадайте число від 1 до 100.")
    while not guessed:
        user_guess = input("Ваш варіант: ")
        attempts += 1
        if user_guess.isdigit():
            user_guess = int(user_guess)
            # з верху зробив Криса Олексій з низу Вус Катерина
            if user_guess == secret_number:
                print(f"Вітаємо! Ви вгадали число {secret_number} за {attempts} спроб.")
                guessed = True
            elif user_guess < secret_number:
                print("Загадане число більше. Спробуйте ще раз.")
            else:
                print("Загадане число менше. Спробуйте ще раз.")
        else:
            print("Будь ласка, введіть дійсне число.")
if __name__ == "main":
    guess_the_number()
