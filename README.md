# Robuste Portfoliooptimierung — Code zur Masterarbeit

Dieses Repository enthält den vollständigen Python-Code zur Masterarbeit
**"Robuste Portfoliooptimierung"** (Marei Peischl, TU Darmstadt, 2026).

Die Implementierung baut auf folgenden drei Arbeiten auf:
- Zhu, S.-S. & Fukushima, M. (2009). *Worst-Case Conditional Value-at-Risk with
  Application to Robust Portfolio Management.* Operations Research, 57(5).
- Huang, D., Zhu, S., Fabozzi, F. J. & Fukushima, M. (2010). *Portfolio Selection
  under Distributional Uncertainty: A Relative Robust CVaR Approach.* European
  Journal of Operational Research, 203(1).
- Kim, J. H., Kim, W. C. & Fabozzi, F. J. (2014). *Recent Developments in Robust
  Portfolios with a Worst-Case Approach.* Journal of Optimization Theory and
  Applications, 161(1).

## Inhalt

| Datei | Kapitel | Beschreibung |
|---|---|---|
| `masterarbeit_paper3.ipynb` | Kapitel 6 | Reproduktion der empirischen Anwendung aus Huang et al. (2010, Abschnitt 4.1): Nominal-CVaR, WCVaR und RCVaR unter multivariater Normalverteilungsannahme (SOCP), Reproduktion von Tabelle 1 und Figure 1, ergänzende Regret-Analyse |
| `masterabreit_daily.ipynb` | Kapitel 7 | Eigene Erweiterung: robuste Portfoliooptimierung unter empirisch nicht-normalverteilten Finanzkrisen-Tagesrenditen (2007–2009), szenariobasiertes LP-Modell unter Box-Unsicherheit |

## Daten

Die verwendeten Renditedaten (30 Industry Portfolios) stammen aus der frei
zugänglichen Datenbibliothek von Kenneth R. French:
https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html

Verwendet wurden:
- *30 Industry Portfolios*, monatliche wertgewichtete Renditen (Kapitel 6)
- *30 Industry Portfolios*, tägliche wertgewichtete Renditen (Kapitel 7)

Die Rohdaten sind aus Lizenzgründen nicht Teil dieses Repositories; sie können
über den obigen Link kostenlos heruntergeladen werden.

## Voraussetzungen

```bash
pip install numpy pandas matplotlib scipy cvxpy
```

Getestet mit CVXPY 1.7.5 und dem Solver ECOS.

## Ausführung

Beide Notebooks sind eigenständig lauffähig. Die jeweilige CSV-Datei (siehe
Abschnitt "Daten") muss im selben Verzeichnis wie das Notebook liegen bzw. der
Pfad in der ersten Code-Zelle entsprechend angepasst werden.
