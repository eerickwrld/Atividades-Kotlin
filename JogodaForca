fun main() {
     val palavraSecreta = "kotlin"
     val letrasDescobertas = MutableList(palavraSecreta.length) { '_' }
     val letrasErradas = mutableListOf<Char>()
     val tentativasMax = 6
     var tentativas = 0
 
     println("🎮 Bem-vindo ao Jogo da Forca!")
     println("Dica: linguagem que você está aprendendo")
 
     while (tentativas < tentativasMax && letrasDescobertas.contains('_')) {
         println("\nPalavra: ${letrasDescobertas.joinToString(" ")}")
         print("Digite uma letra: ")
         val input = readln().lowercase()
 
         if (input.length != 1 || !input[0].isLetter()) {
             println("Digite apenas uma letra.")
             continue
         }
 
         val letra = input[0]
 
         if (letra in letrasDescobertas || letra in letrasErradas) {
             println("Você já tentou essa letra.")
             continue
         }
 
         if (letra in palavraSecreta) {
             for (i in palavraSecreta.indices) {
                 if (palavraSecreta[i] == letra) {
                     letrasDescobertas[i] = letra
                 }
             }
             println("Acertou!")
         } else {
             tentativas++
             letrasErradas.add(letra)
             println("Errou! Tentativas restantes: ${tentativasMax - tentativas}")
         }
 
         println("Letras erradas: ${letrasErradas.joinToString(", ")}")
     }
 
     if (letrasDescobertas.contains('_')) {
         println("\nVocê perdeu! A palavra era: $palavraSecreta")
     } else {
         println("\nParabéns! Você descobriu a palavra: ${letrasDescobertas.joinToString("")}")
     }
 }
