document.addEventListener("DOMContentLoaded", function(){...});:  Ele garante que o código JavaScript dentro dele seja executado apenas quando o DOM estiver pronto para ser manipulado.
Dentro desse evento, são definidos os manipuladores de eventos para os botões de comparar, calcular intervalo e exibir data atual.
let comparar=document.getElementById('comparar');, let intervalo=document.getElementById('intervalo');, let atual=document.getElementById('atual');: Estas linhas recuperam referências para os elementos HTML dos botões "Comparar", "Intervalo" e "Atual", respectivamente, usando seus IDs.
comparar.addEventListener('click', function(){...});, intervalo.addEventListener('click', function(){...});, atual.addEventListener('click', function(){...});: Essas linhas definem funções de callback que serão executadas quando os botões correspondentes forem clicados.
Dentro dessas funções de callback, são realizadas as seguintes operações:
Para o botão "Comparar": são recuperadas as datas inseridas pelo usuário, verificado se são válidas e então comparadas para determinar qual é a maior. Se uma das datas for inválida, é exibido um alerta informando ao usuário.
Para o botão "Intervalo": são recuperadas as datas inseridas pelo usuário, verificado se são válidas e então calculado o intervalo entre elas em dias. Se a primeira data for maior ou igual à segunda, é exibido um alerta informando ao usuário que a primeira data deve ser mais antiga.
Para o botão "Atual": é obtida a data atual do sistema e exibido um alerta com a data formatada.
compararData(data1, data2): Esta função compara duas datas e retorna a data maior entre elas.
intervaloData(data1, data2): Esta função calcula o intervalo em segundos entre duas datas. Se a primeira data for maior ou igual à segunda, um alerta é exibido e a função retorna false.
validar(data1, data2): Esta função verifica se as datas fornecidas são válidas. Se alguma delas for inválida (por exemplo, se não for uma data válida), um alerta é exibido e a função retorna true.
converterData(dataAtual): Esta função converte uma data para uma string no formato "HH:MM - DD/MM/AAAA" e retorna essa string. Ela adiciona zeros à esquerda, se necessário, para garantir que o formato da data seja consistente.
