---
title: Efeitos gráficos
description: Uma lista de recursos que devem ser desabilitados durante a execução como uma sessão remota em um ambiente de Serviços de Área de Trabalho Remota.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f850b8bac5d084419b1f15c2e0efe619da5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916315"
---
# <a name="graphic-effects"></a>Efeitos gráficos

Um servidor de Serviços de Área de Trabalho Remota depende da rede para transmitir todas as entradas e saídas para seus terminais cliente. Consequentemente, os aplicativos que fazem uso excessivo de efeitos gráficos podem afetar o desempenho de todos os clientes Serviços de Área de Trabalho Remota diminuindo a rede. Além disso, a velocidade de transmissão mais lenta em uma rede pode fazer com que esses efeitos especiais pareçam menos agradáveis do que em um ambiente de vídeo local.

Em particular, os aplicativos devem desabilitar ou minimizar o uso dos seguintes recursos ao serem executados em um ambiente de Serviços de Área de Trabalho Remota como uma sessão remota:

-   Telas de abertura — informações gráficas do produto ou da empresa exibidas enquanto um aplicativo está sendo iniciado. A transmissão de uma tela inicial para um cliente Conexão de Área de Trabalho Remota (RDC) consome largura de banda de rede extra e força o usuário a aguardar antes de acessar o aplicativo.
-   Animações, que consomem tempo de CPU e largura de banda de rede.
-   Entrada direta ou saída para a tela. Se você precisar ler bits na tela, mantenha uma cópia separada e fora da tela do buffer de vídeo. Da mesma forma, se você precisar fazer uma saída de tela elaborada — por exemplo, sobrepondo várias imagens para chegar em uma tela de composição final — faça isso funcionar em um buffer fora da tela e, em seguida, envie os resultados para o buffer de vídeo real.

Para obter mais informações sobre como detectar sessões remotas, consulte [detectando o ambiente de serviços de área de trabalho remota](detecting-the-terminal-services-environment.md).

Use a biblioteca Microsoft Foundation Class, ou MFC, sempre que possível. O MFC tem uma longa lista de classes testadas e verdadeiras para executar uma ampla variedade de tarefas. A maioria dessas classes funciona bem em um ambiente de Serviços de Área de Trabalho Remota, geralmente muito melhor do que soluções reprojetadas. Um bom exemplo é a classe que fornece texto de ajuda sensível ao contexto — texto de ajuda que aparece na tela quando o ponteiro do mouse passa sobre um botão ou item de menu. Se um aplicativo usar a implementação do MFC para fornecer esse recurso, ele funcionará razoavelmente bem no sistema de desktop. Mas se o aplicativo implementar esse recurso usando caixas de diálogo ou uma abordagem alternativa, o resultado final poderá não funcionar também em um ambiente de Serviços de Área de Trabalho Remota.

 

 




