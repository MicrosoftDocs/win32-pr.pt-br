---
description: As diretrizes neste tópico destinam-se a ajudá-lo a escrever mensagens de erro claras que são fáceis de localizar e úteis para os clientes.
ms.assetid: 361833e4-b94f-4ef9-a8f5-adf543534a67
title: Diretrizes de mensagem de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1787eabd43d660322577ac766880d76854c574e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646208"
---
# <a name="error-message-guidelines"></a>Diretrizes de mensagem de erro

Uma mensagem de erro é o texto que é exibido para descrever um problema que está impedindo o usuário ou o sistema de concluir uma tarefa. O problema pode resultar em corrupção ou perda de dados. Outros tipos de mensagem incluem confirmações, avisos e notificações. As diretrizes neste tópico destinam-se a ajudá-lo a escrever mensagens de erro claras que são fáceis de localizar e úteis para os clientes.

Mensagens de erro mal gravadas podem ser uma fonte de frustração para os usuários e podem aumentar os custos de suporte técnico. Uma mensagem de erro bem escrita fornece as seguintes informações para o usuário:

-   O que aconteceu e por quê?
-   Qual é o resultado final do usuário?
-   O que o usuário pode fazer para impedir que ele aconteça novamente?

O comprimento do texto não é um problema, contanto que o desenvolvedor manipule tamanhos de buffer corretamente. É importante que o usuário tenha todas as informações necessárias para resolver o problema. Se uma mensagem tiver vários públicos, talvez seja necessário fornecer texto separado para administradores, usuários finais e desenvolvedores.

## <a name="best-practices"></a>Práticas Recomendadas

Veja a seguir as maneiras de melhorar suas mensagens de erro:

-   Evite condições de erro. Se você puder prever que ocorrerá um erro quando um usuário executar uma ação específica, reescreva o código para que o usuário não possa causar o erro.
-   Grave uma mensagem de erro separada para cada causa conhecida do erro. Não use uma única mensagem genérica para explicar cada motivo possível para o erro, a menos que você não possa determinar a causa do erro quando ele ocorrer.
-   Declare o problema claramente e, se for útil para o usuário, explique o que causou o problema. Sempre que possível, substitua as mensagens genéricas dos recursos da tabela de mensagens do sistema por uma mensagem detalhada que é específica para o problema.
-   Forneça ao usuário uma solução para o problema. Se a solução tiver mais de uma etapa, consulte um tópico da ajuda o explica a tarefa em detalhes.
-   Exiba somente o nome do produto, do componente ou do assistente na barra de título da mensagem. Isso ajuda o usuário a determinar onde está o problema. Não resuma o problema na barra de título ou inclua a palavra "erro".
-   Não use um jargão técnico, use a terminologia que seu público compreende. Não use gírias ou abreviações.
-   Use os botões de comando apropriados, como OK, cancelar, sim, não e tentar novamente. Você pode usar combinações desses botões. Os botões Sim e não sempre devem ser usados em combinação e devem sempre ser precedidos por uma pergunta.
    -   Para interromper uma operação e fechar a caixa de mensagem, use o botão **Cancelar** .
    -   Para fechar uma caixa de mensagem, use o botão **fechar** .
    -   Para fornecer mais informações sobre a causa do erro, use o botão **detalhes** .
    -   Para fornecer mais informações sobre a solução para o problema, use o botão **ajuda** .
    -   Se uma ação do usuário for incluída na mensagem, use o botão **OK** para fechar a caixa de mensagem.
    -   **Sim** e **nenhum** botão deve ser usado em combinação e deve sempre ser precedido por uma pergunta.
-   Se o erro for um erro crítico, grave-o no [log de eventos](../eventlog/event-logging.md).

## <a name="style-considerations"></a>Considerações sobre estilo

-   Use frases completas, mas simples.
-   Use o conjugação presente para descrever as condições que causaram o problema ou um estado que ainda existe. Você pode usar conjugação anteriores para descrever um evento distinto que ocorreu no passado.
-   Use o Active Voice sempre que possível. Você pode usar voz passiva para descrever a condição de erro.
-   Evite texto em maiúsculas e pontos de exclamação.
-   Não faça o usuário se sentir com falha mesmo que o problema seja o resultado de um erro do usuário.
-   Não anthropomorphize. Não sudizermos que os programas ou o hardware possam imaginar ou sentir.
-   Não use palavras ou frases uso coloquial. Não use termos que possam ser ofensivos em determinadas culturas.
-   Não compor vários substantivos sem adicionar uma preposição ou subcláusula para esclarecer o significado. Por exemplo, "servidor do diretório do serviço LDAP do servidor do site" deve ser alterado para "servidor de diretório para o serviço LDAP do servidor do site".
-   Insira descritores antes de um termo para esclarecer o significado da frase. Por exemplo, "Especifique InfID quando detectar estiver definido como não." deve ser alterado para "especificar o parâmetro InfID quando a opção Detect for definida como não".
-   Evite a palavra "Bad". Use termos mais descritivos para informar ao usuário o que está errado. Por exemplo, evite mensagens como "tamanho inadequado". Em vez disso, informe ao usuário quais critérios usar ao especificar um tamanho.
-   Evite a palavra "por favor". Ele pode ser interpretado para significar que uma ação necessária é opcional.
-   Coloque palavras que estão no índice e relevantes para o significado central no início da cadeia de caracteres da mensagem.

 

 
