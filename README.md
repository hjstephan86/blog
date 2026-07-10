# fork() in C

Hier ist der Beispielcode für die Nutzung von `fork()`:

```c
#include <stdio.h>
#include <unistd.h> // Hier drin steckt fork()

int main() {
    pid_t pid;

    printf("Vor dem fork... (Das druckt nur das Original)\n");

    // Hier passiert die Spaltung!
    pid = fork();

    if (pid < 0) {
        // Fehlerfall
        fprintf(stderr, "Fork fehlgeschlagen!");
        return 1;
    } 
    else if (pid == 0) {
        // Dieser Block wird NUR vom Kindprozess ausgeführt
        printf("Hallo, ich bin das Kind! Mein fork-Rückgabewert ist: %d\n", pid);
    } 
    else {
        // Dieser Block wird NUR vom Elternprozess ausgeführt
        printf("Hallo, ich bin das Elternteil! Das Kind hat die PID: %d\n", pid);
    }

    printf("Dieser Text wird von BEIDEN gedruckt!\n");
    return 0;
}
```
Wieso wird bei pid = fork(); derselbe Befehl rechts vom = nur vom Elternprozess ausgeführt und links vom = von beiden Prozessen ausgeführt? Das ist etwas willkürluch und nicht klar definiert oder getrennt. Aufgrund dieser Bedeutung sind zum Beispiel unterschiedliche Interpretationen oder Ausführungen denkbar. Es kann zum Beispiel sein, dass beide Prozesse mit einer unterschiedlichen pid weiter ausgeführt werden, nämlich jeder Prozess mit der pid, die er ab dieser Ausführung selber hat. Es kann aber auch sein, dass beide Prozesse mit dieser eindeutigen pid weiter ausgeführt werden, die fork() für alle Prozesse links vom = eindeutig zurückgibt.
