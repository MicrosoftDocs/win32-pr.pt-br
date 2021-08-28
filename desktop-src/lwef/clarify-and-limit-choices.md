---
title: Esclarecer e limitar opções
description: Esclarecer e limitar opções
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7c6371009865baa685e3644c2c1e62e1713bd40a0c64a7a8530b849e813d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480300"
---
# <a name="clarify-and-limit-choices"></a>Esclarecer e limitar opções

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O reconhecimento de fala se torna mais bem-sucedido quando o usuário aprende o intervalo de gramática apropriada. Ele também funciona melhor quando o intervalo de opções é limitado. Quanto menos aberta a entrada, melhor o mecanismo de fala pode analisar a entrada de informações acústicas.

O Microsoft Agent inclui vários provisionamentos integrados que aumentam o sucesso da entrada de fala. A primeira é a Janela Comandos exibida quando o usuário diz "Abrir Janela comandos" ou "What can I say?" (ou quando o usuário escolhe Abrir Janela comandos no menu pop-up do caractere). A Janela Comando serve como um guia visual para a gramática ativa do mecanismo de fala. Ele também reduz os erros de reconhecimento ativando apenas a gramática de fala do aplicativo ativo de entrada e os comandos globais do Microsoft Agent. Portanto, a gramática ativa do mecanismo de fala se aplica ao contexto imediato. Para obter mais informações sobre a janela Comandos, consulte Visão [geral da Interface de Programação do Microsoft Agent.](microsoft-agent-programming-interface-overview.md)

Ao criar comandos habilitados para voz do Microsoft Agent, você pode criar o texto de legenda que aparece na Janela Comandos, bem como seu texto de voz (gramática), as palavras que o mecanismo deve usar para corresponder a esse comando. Sempre tente tornar seus comandos o mais distintos possível. Quanto maior a diferença entre o texto dos comandos, especialmente para o texto de voz, maior a probabilidade de o mecanismo de fala ser capaz de discriminar entre comandos falados e fornecer uma combinação precisa. Evite também comandos de palavra única ou muito curtos. Em geral, informações mais acústicas em um enunciado falado dão ao mecanismo uma chance melhor de fazer uma combinação precisa.

Ao definir o texto de voz para um comando, forneça uma variedade razoável de palavras. Solicitações que significam a mesma coisa podem ser formuladas de maneira muito diferente, conforme ilustrado no exemplo a seguir:

Adicione um pouco de pimentão.

Eu gostaria de um pouco de pimentão.

Você pode adicionar um pouco de pimentão?

Pimentão, por favor.

O Microsoft Agent permite que você especifique facilmente alternativas ou palavras opcionais para a gramática de voz para seu aplicativo. Coloque palavras ou frases alternativas entre parênteses, separadas por um caractere de barra vertical. Você pode definir palavras opcionais, delimitando-as entre caracteres de colchete. Você também pode aninhar alternativas ou palavras opcionais. Além disso, você também pode usar reellipses (...) no texto de voz como um espaço reservado para qualquer palavra. No entanto, o uso de reellips com muita frequência pode dificultar a distinção entre comandos de voz diferentes pelo mecanismo. Em qualquer caso, sempre certifique-se de que o texto de voz inclua pelo menos uma palavra distinta para cada comando que não seja opcional. Normalmente, isso deve corresponder a uma palavra ou palavras no texto de legenda que você define que aparece na Janela Comandos.

Embora você possa incluir símbolos, pontuação ou abreviações no texto da legenda, evite-os em seu texto de voz. Muitos mecanismos de reconhecimento de fala não podem manipular símbolos e abreviações ou podem usá-los para definir parâmetros de entrada especiais. Além disso, os números de ortagem. Isso também garante um suporte de reconhecimento mais confiável.

Você também pode usar prompts de diretiva para evitar a entrada aberta. Os prompts de diretiva referenciam implicitamente as opções ou as instalam explicitamente, conforme mostrado nos exemplos a seguir:



| Prompt                                           | Avaliação                                                    |
|--------------------------------------------|-----------------------------------------------------|
| O que você quer?                          | Muito geral, uma solicitação aberta                  |
| Escolha um estilo de pizza ou um ingredientes.        | Bom, se as opções estão visíveis, mas ainda assim gerais     |
| Diga "Desemão", "Chicago" ou "The Works". | Melhor, uma diretiva explícita com opções específicas |



 

Isso orienta o usuário para a emissão de um comando válido. Ao sugerir as palavras ou frases, é mais provável que você elice o texto esperado em retorno. Para evitar repetições incomuns, altere o texto ou reduza o original para apresentação subsequente à medida que o usuário se torna mais experiente com o estilo de entrada. Os prompts de diretiva também podem ser usados em situações em que o usuário não consegue emitir um comando dentro de um tempo prescrito ou falha ao fornecer um comando esperado. Os prompts de diretiva podem ser fornecidos usando a saída de fala, as interfaces do aplicativo ou ambos. A chave é ajudar o usuário a conhecer as opções apropriadas.

A palavra influencia o sucesso de um prompt. Por exemplo, o prompt "Você gostaria de pedir sua pizza?" pode gerar uma resposta "Sim" ou "Não", mas também pode gerar uma solicitação de pedido. Defina prompts como não ambíguos ou esteja preparado para aceitar uma variedade maior de respostas possíveis. Além disso, observe a tendência das pessoas imitarem palavras e construções que elas escutam. Isso geralmente pode ser usado para ajudar a revogar uma resposta apropriada, como no exemplo a seguir:

**Usuário:** Mostre-me todas as mensagens de Paulo.

**Caractere:**

Isso é mais provável para emitir o nome completo de uma das partes com o prefixo possível de "Quero dizer" ou "Eu quero dizer".

Como os caracteres do Microsoft Agent operam dentro da interface visual do Microsoft Windows, você pode usar elementos visuais para fornecer prompts de diretiva para entrada de fala. Por exemplo, você pode ter o gesto de caractere em uma lista de opções e solicitar que o usuário selecione uma ou exibir opções em uma caixa de diálogo ou janela de mensagem. Isso tem dois benefícios: ele sugere explicitamente as palavras que você deseja que o usuário fale e fornece uma maneira alternativa para o usuário responder.

Você também pode usar outros modos de interação para sugerir aos usuários a gramática de fala apropriada, conforme mostrado no exemplo a seguir:

**Usuário:** (clica na opção de pizza no estilo Decodados com o mouse)

**Caractere:** Pizza no estilo de pizza.

**Usuário:** (clica na opção Queijo Extra com o mouse)

**Caractere:** Adicione "Extra Cheese".

Outro fator importante na entrada de fala bem-sucedida é a indicação do usuário quando o mecanismo está pronto para entrada, pois muitos mecanismos de fala permitem apenas um único enunciado por vez. O Microsoft Agent dá suporte a isso de duas maneiras. Primeiro, se a placa de som for compatível com MIDI, o Microsoft Agent gerará um breve tom para sinalizar quando o canal de entrada de fala estiver disponível. Em segundo lugar, a janela Dica de Escuta exibe um prompt de texto apropriado quando o caractere (mecanismo de fala) está escutando a entrada. Além disso, essa dica exibe o que o mecanismo ouviu.

 

 




