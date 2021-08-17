---
title: Efeitos gráficos
description: Uma lista de recursos que devem ser desabilitados durante a execução como uma sessão remota em um Serviços de Área de Trabalho Remota ambiente.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cad01bb7b61c471ba81f382d1fc4031b8c44dcef63a78c5a0cc17641b5e457e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059434"
---
# <a name="graphic-effects"></a>Efeitos gráficos

Um Serviços de Área de Trabalho Remota conta com a rede para transmitir toda a entrada e saída para seus terminais de cliente. Consequentemente, os aplicativos que fazem uso excessivo de efeitos gráficos podem afetar o desempenho de todos os Serviços de Área de Trabalho Remota clientes, retardando a rede. Além disso, a velocidade de transmissão mais lenta em uma rede pode fazer com que esses efeitos especiais pareçam menos desagradados do que seriam em um ambiente de vídeo local.

Em particular, os aplicativos devem desabilitar ou minimizar o uso dos seguintes recursos ao executar em um ambiente Serviços de Área de Trabalho Remota como uma sessão remota:

-   Telas instaladas — informações gráficas do produto ou da empresa exibidas enquanto um aplicativo está iniciando. Transmitir uma tela inicial para um cliente RDC (Conexão de Área de Trabalho Remota) consome largura de banda de rede extra e força o usuário a aguardar antes de acessar o aplicativo.
-   Animações, que consomem tempo de CPU e largura de banda de rede.
-   Entrada direta ou saída para a tela. Se você precisar ler bits da tela, mantenha uma cópia separada e fora da tela do buffer de vídeo. Da mesma forma, se você precisar elaborar a saída da tela, por exemplo, sobrepor várias imagens para chegar a uma tela composta final, faça esse trabalho em um buffer fora da tela e, em seguida, envie os resultados para o buffer de vídeo real.

Para obter mais informações sobre como detectar sessões remotas, consulte [Detecting the Serviços de Área de Trabalho Remota Environment](detecting-the-terminal-services-environment.md).

Use a biblioteca do Microsoft Foundation Class, ou MFC, sempre que possível. O MFC tem uma longa lista de classes tentadas e verdadeiras para executar uma ampla variedade de tarefas. A maioria dessas classes funciona bem em um ambiente de Serviços de Área de Trabalho Remota, geralmente muito melhor do que soluções de engenharia. Um bom exemplo é a classe que fornece texto de ajuda contextitivo – texto de ajuda que aparece na tela quando o ponteiro do mouse sobre um botão ou item de menu. Se um aplicativo usar a implementação do MFC para fornecer esse recurso, ele funcionará razoavelmente bem no sistema da área de trabalho. Mas se o aplicativo implementar esse recurso usando caixas de diálogo ou uma abordagem alternativa, o resultado final poderá não funcionar bem em um ambiente de Serviços de Área de Trabalho Remota.

 

 




