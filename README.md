# Ausgangslage
Die private Cloud der Bundesverwaltung (BV) umfasst verschiedene Dienstleistungen und Plattformen. Das BIT stellt grundsätzlich die Infrastruktur zur Verfügung in Form von IaaS und PaaS. Die Fachanwendungsbetreiber haben jedoch teils erhöhte Sicherheitsanforderungen, wozu private Infrastrukturen benötigt werden. Ziel des BIT ist jedoch die allermeistens Applikationen auf gut geschützter aber geteilter Infrastruktur zu betreiben um Kosten zu sparen.

# Problemstellung
Die Sicherheitsanforderungen der Fachanwendungen entstehen oft aus Standards/Richtlinien/Normen der BV welche manuell und plattformspezifisch umgesetzt werden. Die daraus resultierenden Regeln werden oft unterschiedlich definiert, abgelegt und angewendet. Zusätzlich besteht die Gefahr, dass Standards/Richtlinien/Normen der BV unterschiedlich interpretiert werden können und somit dann andere Regeln angewendet werden.
Es braucht eine Möglichkeit, Standards/Richtlinien/Normen der BV konsistent und effizient über die verschiedenen Plattformen hinweg zu deklarieren. Wenn Fachanwendungen oder Anwendungsteile niedrigere Sicherheitsanforderungen vorweisen, können diese auch auf geteilter Infrastruktur betrieben werden.
Dieselbe Problemstellung lässt sich auch anwenden auf die Hybrid [Multi-Cloud Strategie der BV](https://www.bk.admin.ch/bk/de/home/digitale-transformation-ikt-lenkung/bundesarchitektur/cloud.html) und deren Umsetzung in der Swiss Government Cloud (SGC) an, wobei dies hier out of Scope gelassen wird.

# Ziele
  *   Es soll ein Framework entworfen werden, welches erlaubt die (Sicherheits-) Anforderungen von Anwendungen und Anwendungsteilen deklarativ und einheitlich definiert werden können.
  *   Das Framework soll in der Lage sein Reports auszugeben mit Informationen zur Einhaltung sowie Nichteinhaltung der Regeln/… .
  *   Das Framework soll eine Möglichkeit bieten, neu zu deployende Anwendungen auf die Einhaltung zu prüfen und bei Nichteinhaltung entsprechende Folgeaktionen (z.B. Berichterstattung, Behebung) auszulösen.
  *   Die Regeln sollen zentral abgelegt werden und somit eine single Source of Truth darstellen können.
  *   Der Syntax des deklarativen Codes (IaC) soll intuitiv lesbar sein sowohl auch anwendbar durch Automatismen.

# Herausforderungen
  *   Das Regelwerk soll ein hohes Mass an Flexibilität und Erweiterbarkeit aufweisen um eine Anwendbarkeit auf nicht-Kubernetes Infrastruktur nicht auszuschliessen.
  *   Das resultierende Regelwerk soll in die bestehende Infrastruktur integriert werden können.

# Techhnologie / fachliche Schwerpunkte
  *   Public Cloud / Hybrid Cloud
  *   Infrastructure as Code
