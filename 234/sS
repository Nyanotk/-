import random

def buble_sort(arr):
    count_if = 0
    count_move = 0
    for i in range(len(arr) - 1):
        is_sorted = True  
        for j in range(len(arr) - i - 1):
            count_if += 1
            if arr[j] > arr[j + 1]:
                count_move += 1
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                is_sorted = False
        if is_sorted:
            break  
    return arr, count_if, count_move

def selection_sort(arr):
    count_if = 0
    count_move = 0
    for i in range(len(arr)):
        minimum = i
        for j in range(i + 1, len(arr)):
            count_if += 1
            if arr[j] < arr[minimum]:
                minimum = j
        count_move += 1
        arr[minimum], arr[i] = arr[i], arr[minimum]
    return arr, count_if, count_move

n_arr = [14, 28, 56, 112, 224, 448, 896]

for n in n_arr:
    arr = [random.randint(-100, 100) for _ in range(n)]
    print("Исходный массив:", arr)
    print("======Количество элементов======", n)
    arr, count_if, count_move = buble_sort(arr.copy())
    print("Пузырьковая сортировка:", arr)
    print(f"Количество сравнений: {count_if}, Количество перестановок: {count_move}")
    arr, count_if, count_move = selection_sort(arr.copy())
    print("Сортировка выбором:", arr)
    print(f"Количество сравнений: {count_if}, Количество перестановок: {count_move}")
    input('Чтобы продолжить, нажмите Enter\n')

comparisons_bubble = []
swaps_bubble = []
comparisons_selection = []
swaps_selection = []

for n in n_arr:
    arr = [random.randint(-100, 100) for _ in range(n)]
    _, count_if, count_move = buble_sort(arr.copy())
    comparisons_bubble.append(count_if)
    swaps_bubble.append(count_move)
    _, count_if, count_move = selection_sort(arr.copy())
    comparisons_selection.append(count_if)
    swaps_selection.append(count_move)