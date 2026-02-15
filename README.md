# 📊 Executive Sales & Profitability Dashboard - Power BI

## 📝 Project Overview
Kompleksowy dashboard analityczny stworzony w Power BI, mający na celu przekształcenie surowych danych transakcyjnych (Superstore Dataset) w czytelne i interaktywne narzędzie dla kadry zarządzającej. Raport skupia się na monitorowaniu kluczowych wskaźników efektywności (KPI), trendów czasowych oraz identyfikacji obszarów generujących straty.

![Main Dashboard Overview](dashboard.jpg)
---

## 🚀 Key Features
* **Dynamiczne KPI:** Śledzenie łącznej sprzedaży, zysku, liczby zamówień oraz średniego czasu realizacji zamówienia.
* **Analiza Trendów (Sales & Profit over Time):** Wykres kombinowany (słupki + linia) pokazujący korelację między przychodem a zyskiem z płynną, ciągłą osią czasu.
* **Analiza Rentowności Regionalnej:** Szczegółowa tabela z formatowaniem warunkowym (Heatmap), pozwalająca na natychmiastową lokalizację strat w konkretnych kategoriach i regionach.
* **Scatter Plot Analysis:** Wizualizacja zależności między wysokością rabatu a marżą zysku, ułatwiająca optymalizację polityki rabatowej.
* **Analiza Struktury Zysku (Waterfall Chart):** Przedstawienie wkładu poszczególnych kategorii produktów w końcowy wynik finansowy.

---

## 🛠 Tech Stack & Solutions
W trakcie projektu rozwiązałem szereg wyzwań technicznych, które znacząco poprawiły UX i czytelność danych:

### 1. Optymalizacja Osi Czasu (DAX & Power Query)
Początkowy widok dzienny był nieczytelny i zawierał paski przewijania. Zastosowałem grupowanie do miesięcy, aby uzyskać płynny trend bez utraty ciągłości osi.
> **Kod kolumny obliczeniowej:**
> `Miesiac = STARTOFMONTH('Superstore'[Order Date])`

### 2. Zaawansowane Formatowanie KPI
Standardowe zaokrąglenia Power BI (np. "10K") były mało precyzyjne dla liczby zamówień. Stworzyłem dedykowaną miarę DAX, wymuszając format liczby całkowitej z separatorem tysięcy.
> **Formuła miary:**
> `Number of Orders = COUNT('Superstore'[Order ID])`

---

## 💡 Key Business Insights
* **Pułapka Rabatów:** Dane wyraźnie pokazują, że rabaty powyżej 20% drastycznie obniżają marżę, rzadko przekładając się na adekwatny wzrost wolumenu.
* **Problematyczne Kategorie:** Region *Central* wykazuje znaczące straty w kategoriach *Tables* i *Bookcases*, co sugeruje konieczność rewizji łańcucha dostaw lub cen w tym obszarze.

---

## 📂 How to use
1. Pobierz plik `.pbix` z głównego folderu repozytorium.
2. Otwórz projekt w **Power BI Desktop**.
3. Skorzystaj z panelu filtrów po lewej stronie, aby dynamicznie zmieniać zakres dat, regiony lub segmenty klientów.

