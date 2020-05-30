// Introdução JavaScript

// Exercício 1 

/*  Crie uma função que dado o objeto a seguir:
    var endereco = {
    rua: "Rua dos pinheiros",
    numero: 1293,
    bairro: "Centro",
    cidade: "São Paulo",
    uf: "SP"
    };
    Retorne o seguinte conteúdo:
    O usuário mora em São Paulo / SP, no bairro Centro, na rua "Rua dos Pinheiros" com
    nº 1293. */
    
  var endereco = {
                rua: "Rua dos Pinheiros",
                numero: 1293,
                bairro: "centro",
                cidade: "São Paulo",
                uf: "SP"
            }

            function dados(end) {
                return "O usuário mora em " + end.cidade + " / " + end.uf + " no bairro " + end.bairro + ", na " 
                + end.rua + " com n° " + end.numero + ".";
            }

            console.log(dados(endereco))
            
            
// Exercício 2
  
  /*  Crie uma função que dado um intervalo (entre x e y) exiba todos número pares:
      function pares(x, y) {
      // código aqui
       }
      pares(32, 321); */
    
      function pares(x, y) {
                    for (var i=x; (i % 2) == 0  && i<=y; i++) {
                        console.log(i)
                        i++
                    }
                }
                pares(32, 321);
                
// Exercício 3

  /*  Escreva uma função que verifique se o vetor de habilidades passado possui a habilidade "Javascript"
      e retorna um booleano true/false caso exista ou não.
    
      function temHabilidade(skills) {
      // código aqui
      }
      var skills = ["Javascript", "ReactJS", "React Native"];
      temHabilidade(skills); // true ou false
      Dica: para verificar se um vetor contém um valor, utilize o método indexOf.*/
      
       function temHabilidade(skills) { 
             return skills.indexOf("Javascript")>=0 
             }
            var skills = ["Javascript", "ReactJS", "React Native"];
            temHabilidade(skills);
 
 // Exercício 4
    /*  Escreva uma função que dado um total de anos de estudo retorna o quão experiente o usuário é:
        function experiencia(anos) {
        // código aqui
        }
        var anosEstudo = 7;
        experiencia(anosEstudo);
        // De 0-1 ano: Iniciante
        // De 1-3 anos: Intermediário
        // De 3-6 anos: Avançado
        // De 7 acima: Jedi Master
        
        function experiencia(anos) {
               var resultado;
               switch(true) {
                    case (anos < 1):
                    resultado = "Iniciante";
                    break;
                    case (anos < 3):
                    resultado = "Intermediário";
                    break;
                    case (anos < 7):
                    resultado = "Avançado";
                    break;
                    case (anos >= 7):
                    resultado = "Jedi Master";
                    break;
                }
                console.log(resultado)
                return resultado;
            }
            var anosEstudo = 7;
            console.log(experiencia(anosEstudo));
            
// Exercício 5
   /* Dado o seguinte vetor de objetos:
      v
      Escreva uma função que produza o seguinte resultado:
      O Diego possui as habilidades: Javascript, ReactJS, Reduxar usuarios = [
       {
       nome: "Diego",
       habilidades: ["Javascript", "ReactJS", "Redux"]
       },
       {
       nome: "Gabriel",
       habilidades: ["VueJS", "Ruby on Rails", "Elixir"]
       }
      ];
      O Gabriel possui as habilidades: VueJS, Ruby on Rails, Elixir
      Dica: Para percorrer um vetor você deve utilizar a sintaxe for...of e para unir valores de um array
      com um separador utilize o join.*/
      
       var usuarios = [
            {
            nome: "Diego",
            habilidades: ["Javascript", "ReactJS", "Redux"]
            },
            {
            nome: "Gabriel",
            habilidades: ["VueJS", "Ruby on Rails", "Elixir"]
            }
            ];
            
            function escreva (x) {
                var busca;
                for (busca of x) {
                    console.log("O "+ busca.nome + 
                    " possui as habilidades: "
                    + busca.habilidades.join(", ") + ".")
                }
            } 

            escreva(usuarios)
        
        
    
    
