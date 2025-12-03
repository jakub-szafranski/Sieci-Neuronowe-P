# 🧠 Knowledge Distillation przy brakujących klasach

Projekt z przedmiotu: Sieci Neuronowe (Zima 2025/26)
Autorzy: Weronika Domczewska, Jakub Szafrański, Patryk Wawrzacz

## 📌 Opis projektu

Celem projektu jest zbadanie, czy zjawisko destylacji wiedzy (knowledge distillation) może umożliwić nauczenie modelu ucznia rozpoznawania brakującej klasy, mimo że dane treningowe tej klasy nie są dostępne.

Inspiracją jest praca “Subliminal Learning: Language Models Transmit Behavioral Traits via Hidden Signals in Data”, która sugeruje, że modele mogą przekazywać ukryte sygnały pozwalające odtwarzać informacje niewystępujące bezpośrednio w danych. W naszym projekcie sprawdzamy, czy podobny mechanizm działa również w przypadku sieci neuronowych klasyfikujących obrazy.

## 🎯 Cel badawczy

Wytrenować model nauczyciela na pełnym zbiorze danych (MNIST, CIFAR-10).

Wytrenować model ucznia na zbiorze pozbawionym jednej z klas, korzystając wyłącznie z etykiet pochodzących od nauczyciela.

Sprawdzić, czy uczeń:

- jest w stanie odtworzyć reprezentację brakującej klasy,

- potrafi ją poprawnie klasyfikować,

- wykorzystuje ukryte sygnały z procesu destylacji.

Badamy dwa typy destylacji:

- Soft-label distillation — uczeń otrzymuje pełny rozkład prawdopodobieństwa z modelu nauczyciela.

- Hard-label distillation — uczeń dostaje jedynie finalne predykcje nauczyciela.

## Zbiory danych

- MNIST

- CIFAR-10

## Wybrane rodzaje sieci neuronowych

- FFN 

- CNN (ResNet18)

## 🛠️ Wykorzystywane narzędzia

TensorFlow
scikit-learn


## 📚 Przegląd literatury

Projekt opiera się na pracach dotyczących:

- destylacji wiedzy (Hinton et al., 2015),

- metod data-free KD (Chen et al., Ye et al., Micaelli & Storkey, Yin et al., Nayak et al.),

- dyfuzji ukrytych sygnałów w modelach językowych (Cloud et al., 2025),

- destylacji wiedzy dla niezrównoważonych zbiorów danych (Fujiwara, 2024).


## Instalacja bibliotek

Aby zainstalować wymagane zależności, uruchom:

```bash
pip install torchvision numpy matplotlib scikit-learn tqdm -q


