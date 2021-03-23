---
title: Design de filosofia de filas de comando e listas de comandos
description: As metas de habilitar a reutilização do trabalho de renderização e do dimensionamento multithread, exigiam alterações fundamentais em como os aplicativos do Direct3D enviam o trabalho de renderização para a GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- lista de comandos
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103445"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Design de filosofia de filas de comando e listas de comandos

As metas de habilitar a reutilização do trabalho de renderização e do dimensionamento multithread, exigiam alterações fundamentais em como os aplicativos do Direct3D enviam o trabalho de renderização para a GPU. No Direct3D 12, o processo de envio do trabalho de renderização difere de versões anteriores de três maneiras importantes:

<dl> 1. Eliminação do contexto imediato. Isso habilita o multithreading.  
2. Os aplicativos agora têm como as chamadas de renderização são agrupadas em itens de trabalho da GPU (unidade de processamento gráfico). Isso permite reutilização.  
3. Os aplicativos agora controlam explicitamente quando o trabalho é enviado para a GPU. Isso habilita os itens 1 e 2.  
</dl>

-   [Remoção do contexto imediato](#removal-of-the-immediate-context)
-   [Agrupamento de itens de trabalho da GPU](#grouping-of-gpu-work-items)
-   [Envio de trabalho de GPU](#gpu-work-submission)
-   [Tópicos relacionados](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Remoção do contexto imediato

A maior alteração do Microsoft Direct3D 11 para o Microsoft Direct3D 12 é que não há mais um contexto único e imediato associado a um dispositivo. Em vez disso, para renderizar, os aplicativos criam listas de comandos nas quais as APIs de renderização tradicionais podem ser chamadas. Uma lista de comandos é semelhante ao método Render de um aplicativo do Direct3D 11 que usava o contexto imediato, pois ele contém chamadas que desenham primitivos ou alteram o estado de renderização. Como contextos imediatos, cada lista de comandos não está livre de threads; no entanto, várias listas de comandos podem ser registradas simultaneamente, o que aproveita os processadores modernos de vários núcleos.

As listas de comandos são normalmente executadas uma vez. No entanto, uma lista de comandos pode ser executada várias vezes se o aplicativo garante que as execuções anteriores sejam concluídas antes de enviar novas execuções. Para obter mais informações sobre sincronização de lista de comandos, consulte [executando e sincronizando listas de comandos](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Agrupamento de itens de trabalho da GPU

Além das listas de comandos, o Direct3D 12 aproveita a funcionalidade presente em todos os hardwares hoje, adicionando um segundo nível de listas de comandos, que são chamadas de *pacotes*. Para ajudar a distinguir esses dois tipos, as listas de comandos de primeiro nível podem ser referidas como *listas de comandos diretos*. A finalidade dos pacotes é permitir que os aplicativos agrupem um pequeno número de comandos de API para depois, repetidas execuções de dentro de listas de comandos diretas. No momento da criação de um pacote, o driver executará o máximo de pré-processamento possível para tornar a execução mais eficiente. Os grupos podem ser executados em várias listas de comandos e várias vezes na mesma lista de comandos.

A reutilização de pacotes é um grande driver de eficiência aprimorada com threads de CPU única. Como os pacotes são pré-processados e podem ser enviados várias vezes, há certas restrições em quais operações podem ser executadas em um pacote. Para obter mais informações, consulte [criando e gravando listas de comandos e pacotes](recording-command-lists-and-bundles.md).

## <a name="gpu-work-submission"></a>Envio de trabalho de GPU

Para executar o trabalho na GPU, um aplicativo deve enviar explicitamente uma lista de comandos para uma fila de comandos associada ao dispositivo Direct3D. Uma lista de comandos diretas pode ser enviada para execução várias vezes, mas o aplicativo é responsável por garantir que a lista de comandos diretas concluiu a execução na GPU antes de enviá-la novamente. Os grupos não têm restrições de uso simultâneos e podem ser executados várias vezes em várias listas de comandos, mas os pacotes não podem ser enviados diretamente a uma fila de comandos para execução.

Qualquer thread pode enviar uma lista de comandos a qualquer fila de comandos a qualquer momento e o tempo de execução serializará automaticamente o envio da lista de comandos na fila de comandos, preservando a ordem de envio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




