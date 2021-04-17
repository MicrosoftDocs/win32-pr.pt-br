---
title: Esclarecer e limitar opções
description: Esclarecer e limitar opções
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ed5f95c2e516f304ffa28bcca1d9fd67a9169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798549"
---
# <a name="clarify-and-limit-choices"></a>Esclarecer e limitar opções

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O reconhecimento de fala se torna mais bem-sucedido quando o usuário aprende o intervalo de gramática apropriada. Ele também funciona melhor quando o intervalo de opções é limitado. Quanto menos aberto a entrada, melhor o mecanismo de fala pode analisar a entrada de informações acústica.

O Microsoft Agent inclui várias disposições internas que aumentam o sucesso da entrada de fala. A primeira é a janela comandos exibida quando o usuário diz, "abrir a janela de comandos" ou "o que eu posso dizer?" (ou quando o usuário escolhe abrir a janela de comandos no menu pop-up do caractere). A janela comando serve como um guia visual para a gramática ativa do mecanismo de fala. Ele também reduz os erros de reconhecimento ativando apenas a gramática de fala do aplicativo de entrada-ativo e os comandos globais do Microsoft Agent. Portanto, a gramática ativa do mecanismo de fala aplica-se ao contexto imediato. Para obter mais informações sobre a janela de comandos, consulte [visão geral da interface de programação do Microsoft Agent](microsoft-agent-programming-interface-overview.md).

Quando você cria comandos habilitados para Microsoft Agent Voice, pode criar o texto de legenda que aparece na janela comandos, bem como seu texto de voz (gramática), as palavras que o mecanismo deve usar para corresponder a esse comando. Sempre tente tornar seus comandos tão distintivos quanto possível. Quanto maior a diferença entre a palavra de comandos, especialmente para o texto de voz, mais provável será que o mecanismo de fala seja capaz de discriminar várias entre os comandos falados e forneça uma correspondência precisa. Evite também comandos de palavras simples ou muito curtas. Em geral, mais informações acústicas em um expressão falado proporcionam ao mecanismo uma melhor chance de fazer uma correspondência precisa.

Ao definir o texto de voz para um comando, forneça uma variedade razoável de palavras. As solicitações que significam a mesma coisa podem ser frases de forma muito diferente, conforme ilustrado no exemplo a seguir:

Adicione algumas pepperoni.

Eu gostaria de alguma pepperoni.

Você poderia adicionar algum pepperoni?

Pepperoni, por favor.

O Microsoft Agent permite que você especifique facilmente alternativas ou palavras opcionais para a gramática de voz do seu aplicativo. Você coloca palavras ou frases alternativas entre parênteses, separados por um caractere de barra vertical. Você pode definir palavras opcionais ao colocá-las entre caracteres de colchetes. Você também pode aninhar alternativas ou palavras opcionais. Além disso, você também pode usar reticências (...) em texto de voz como um espaço reservado para qualquer palavra. No entanto, o uso de reticências com muita frequência pode dificultar a distinção entre comandos de voz diferentes. Em qualquer caso, sempre certifique-se de que o texto de voz inclui pelo menos uma palavra distinta para cada comando que não é opcional. Normalmente, isso deve corresponder a uma palavra ou palavras no texto de legenda que você define que aparece na janela de comandos.

Embora você possa incluir símbolos, pontuação ou abreviações no texto da legenda, evite-os no texto de voz. Muitos mecanismos de reconhecimento de fala não podem manipular símbolos e abreviações ou podem usá-los para definir parâmetros de entrada especiais. Além disso, soletrar números. Isso também garante um suporte de reconhecimento mais confiável.

Você também pode usar os prompts de diretiva para evitar a entrada aberta. Os prompts de diretiva referenciam implicitamente as opções ou as Estados explicitamente, conforme mostrado nos exemplos a seguir:



|                                            |                                                     |
|--------------------------------------------|-----------------------------------------------------|
| O que você quer?                          | Muito geral, uma solicitação aberta                  |
| Escolha um estilo ou ingrediente de pizza.        | Bom, se as escolhas estiverem visíveis, mas ainda gerais     |
| Digamos "havaiano", "Chicago" ou "o Works". | Melhor, uma diretiva explícita com opções específicas |



 

Isso orienta o usuário na emissão de um comando válido. Ao sugerir as palavras ou a frase, é mais provável que você extrairá as palavras esperadas no retorno. Para evitar a repetição não natural, altere as palavras ou diminua o original da apresentação subsequente à medida que o usuário se tornar mais experiente com o estilo de entrada. Os prompts de diretiva também podem ser usados em situações em que o usuário não pode emitir um comando dentro de um tempo prescrito ou não fornecer um comando esperado. Os prompts de diretiva podem ser fornecidos usando a saída de fala, suas interfaces de aplicativo ou ambos. A chave está ajudando o usuário a saber as opções apropriadas.

O texto influencia o sucesso de um prompt. Por exemplo, o prompt "gostaria de pedir sua pizza?" pode gerar uma resposta "Sim" ou "não", mas também pode gerar uma solicitação de pedido. Defina os prompts como não ambíguos ou estejam preparados para aceitar uma grande variedade de respostas possíveis. Além disso, observe a tendência de que as pessoas imitam palavras e construções que ouvem. Isso geralmente pode ser usado para ajudar a evocar uma resposta apropriada, como no exemplo a seguir:



|            |                                 |
|------------|---------------------------------|
| Usuário:      | Mostre-me todas as mensagens do Paul. |
| Espaço |                                 |



 

Isso tem mais probabilidade de extrair o nome completo de uma das partes com o prefixo possível de "I mean" ou "Eu queria".

Como os caracteres do Microsoft Agent operam na interface visual do Microsoft Windows, você pode usar elementos visuais para fornecer prompts de diretiva para entrada de fala. Por exemplo, você pode ter o gesto de caractere em uma lista de opções e solicitar que o usuário selecione uma ou exibir opções em uma caixa de diálogo ou janela de mensagem. Isso tem dois benefícios: ele sugere explicitamente as palavras que você deseja que o usuário fale e fornece uma maneira alternativa para o usuário responder.

Você também pode usar outros modos de interação para sugerir sutilmente aos usuários a gramática de fala apropriada, conforme mostrado no exemplo a seguir:



|            |                                                     |
|------------|-----------------------------------------------------|
| Usuário:      | (Clica na opção de pizza estilo havaiano com o mouse) |
| Espaço | Pizza estilo havaiano.                               |
| Usuário:      | (Clica em opção de queijo extra com o mouse)         |
| Espaço | Adicione "queijo extra".                                 |



 

Outro fator importante na entrada de fala bem-sucedida é advertência o usuário quando o mecanismo está pronto para entrada, porque muitos mecanismos de fala permitem apenas um único expressão de cada vez. O Microsoft Agent oferece suporte para isso de duas maneiras. Primeiro, se a placa de som der suporte a MIDI, o Microsoft Agent gerará um breve Tom a ser sinalizado quando o canal de entrada de fala estiver disponível. Em segundo lugar, a janela da dica de escuta exibe um prompt de texto apropriado quando o caractere (mecanismo de fala) está ouvindo a entrada. Além disso, essa dica exibe o que o mecanismo ouviu.

 

 




