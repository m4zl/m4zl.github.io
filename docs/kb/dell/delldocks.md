# <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Dell-Logo.svg/1280px-Dell-Logo.svg.png" alt="drawing" width="350"/>
***

## Zurücksetzen der Dockingstation 

1. Entfernen Sie das USB-C- oder Thunderbolt-Kabel vom Computer.
2. Trennen Sie die Netzstromversorgung von der Dockingstation der WD19 Serie.
3. Leiten Sie eventuell noch vorhandenen Reststrom von der Dockingstation ab, indem Sie den Netzschalter 30 Sekunden lang gedrückt halten.
4. Schließen Sie das Netzkabel an die Dockingstation an.
5. Die LED am Netzschalter der Dockingstation sollte drei (3) Mal blinken.
6. Schließen Sie das USB-C- oder Thunderbolt-Kabel wieder an den Computer an.

## Bios Einstellungen für Typ-C Dockingstationen

1. Gehen Sie zu `System Configuration` und anschließend zu `USB Configuration`.
2. Wählen Sie die Optionen `Enable USB Boot Support` (Unterstützung für Starten von USB aktivieren) und `Enable External USB Port` (Externen USB-Anschluss aktivieren).
3. Navigieren Sie zu `Dell Type-C Dock Configuration` und wählen Sie `Always Allow Dell Docks` aus.
4. Navigieren Sie unter System Configuration zu `USB Power Share` und aktivieren Sie diese Option.
5. Navigieren Sie zu `Thunderbolt Adapter Configuration` und wählen Sie `Enable Thunderbolt Technology Support`, `Enable Thunderbolt Adapter Boot Support` und `Enable Thunderbolt Adapter Preboot Modules`.
6. Wählen Sie in der gleichen Kategorie `Security Level - No Security `(Sicherheitsstufe "keine Sicherheit") aus.
> *HINWEIS: Die Elemente 5 und 6 gelten nur für Computer mit Thunderbolt-Controllern.*
7. Navigieren Sie jetzt zu `POST Behavior` und `Fastboot`. Wählen Sie `Thorough` (Vollständig).
8. Klicken Sie unten rechts auf die Schaltfläche `Apply`, um die vorgenommenen Änderungen zu speichern. Beenden Sie das BIOS, indem Sie auf die Schaltfläche `Exit (Verlassen)` klicken.