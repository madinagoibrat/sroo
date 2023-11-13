import numpy as np

def algorithm1(dataset):
    # Алгоритм 1 коды
    processed_data = dataset * 2
    return processed_data

def algorithm2(processed_data, ground_truth):
    # Алгоритм 2 абсолютті қатені есептеу коды
    absolute_error = np.abs(processed_data - ground_truth)
    return absolute_error

def quasi_linear_composition(dataset, ground_truth):
    # Бүкіл деректер жиынтығы үшін 1 алгоритмін орындаңыз
    processed_data = algorithm1(dataset)

    # Өңделген деректер мен негізгі шындықты пайдаланып 2 алгоритмін орындаңыз
    absolute_error = algorithm2(processed_data, ground_truth)

    return processed_data, absolute_error

# Деректер жиынтығының мысалы және негізгі шындық
dataset = np.array([1, 2, 3, 4, 5])
ground_truth = np.array([10, 12, 14, 16, 18])

# Квази сызықты композицияны орындаңыз
processed_data, absolute_error = quasi_linear_composition(dataset, ground_truth)

# Нәтижелерді басып шығарыңыз
print(f"Processed Data: {processed_data}")
print(f"Absolute Error: {absolute_error}")
