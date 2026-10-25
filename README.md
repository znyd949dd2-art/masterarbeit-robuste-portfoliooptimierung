# Robuste Portfolio-Optimierung — Code zur Masterarbeit
 
Dieses Repository enthält den Python-Code zur Masterarbeit
**„Robuste Portfolio-Optimierung: Theorie, Implementierung und empirische
Evaluation robuster CVaR-Modelle“**
  
## Inhalt
 
- `masterarbeit_kapitel6.ipynb`  (Kapitel 6): Reproduktion der empirischen Anwendung aus Huang et al. (2010, Abschnitt 4.1) mit gleichgewichteten Monatsrenditen 1997–2006: nominales CVaR-, WCVaR- und RCVaR-Modell unter multivariater Normalverteilung (SOCP), Reproduktion von Tabelle 1 und Abbildung 1, Zerlegung des CVaR und Regret je Experte
  
- `masterarbeit_kapitel7.ipynb` (Kapitel 7): Erweiterung auf die Finanzkrise 2007–2009 mit wertgewichteten Tagesrenditen: drei Marktphasen als Experten, szenariobasierte WCVaR- und RCVaR-Modelle als lineare Programme über der endlichen Expertenmenge, Vergleich mit konvexer Hülle und Box-Unsicherheitsmenge, Vergleich mit der Normalverteilungsannahme (SOCP) sowie Robustheit gegenüber den Phasengrenzen 
 
## Daten

- `30_Industry_Portfolios.csv` (Kapitel 6) und `30_Industry_Portfolios_Daily.csv`  (Kapitel 7) 
- `30_Industry_Portfolios_202605.csv`  (Kapitel 6, optional) - ältere Version der Monatsdaten für den Versionsvergleich
 
 
## Voraussetzungen
 
```bash
pip install numpy pandas scipy matplotlib cvxpy ecos
```
 
Verwendet wurden Python 3.9 und CVXPY 1.7.5 mit dem Solver ECOS.
 
## Ausführung
 
Die CSV-Dateien in dasselbe Verzeichnis wie die Notebooks legen (oder den Pfad
über `CSV_PATH` in der ersten Codezelle anpassen) und alle Zellen von oben nach
unten ausführen (*Run All*). Beide Notebooks sind unabhängig voneinander lauffähig.
