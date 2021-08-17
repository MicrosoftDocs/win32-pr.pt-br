---
title: Filosofia de design de filas de comando e listas de comando
description: As metas de permitir a reutilização do trabalho de renderização e do dimensionamento multi-threaded exigiram alterações fundamentais em como os aplicativos Direct3D enviam trabalho de renderização para a GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- lista de comandos
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08f996f3de54b63668d44122929feb4fdbef4380fb8b2f7bb1458f50fe274ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124214"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Filosofia de design de filas de comando e listas de comando

As metas de permitir a reutilização do trabalho de renderização e do dimensionamento multi-threaded exigiram alterações fundamentais em como os aplicativos Direct3D enviam trabalho de renderização para a GPU. No Direct3D 12, o processo de envio de trabalho de renderização é diferente das versões anteriores de três maneiras importantes:

<dl> 1. Eliminação do contexto imediato. Isso habilita o multi-threading.  
2. Os aplicativos agora têm como as chamadas de renderização são agrupadas em itens de trabalho de GPU (unidade de processamento gráfico). Isso permite o re uso.  
3. Os aplicativos agora controlam explicitamente quando o trabalho é enviado para a GPU. Isso habilita os itens 1 e 2.  
</dl>

-   [Remoção do contexto imediato](#removal-of-the-immediate-context)
-   [Agrupar itens de trabalho de GPU](#grouping-of-gpu-work-items)
-   [Envio de trabalho de GPU](#gpu-work-submission)
-   [Tópicos relacionados](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Remoção do contexto imediato

A maior alteração do Microsoft Direct3D 11 para o Microsoft Direct3D 12 é que não há mais um único contexto imediato associado a um dispositivo. Em vez disso, para renderizar, os aplicativos criam listas de comandos nas quais as APIs de renderização tradicionais podem ser chamadas. Uma lista de comandos é semelhante ao método de renderização de um aplicativo Direct3D 11 que usou o contexto imediato em que contém chamadas que desenham primitivos ou alteram o estado de renderização. Assim como contextos imediatos, cada lista de comandos não é de thread livre; no entanto, várias listas de comandos podem ser registradas simultaneamente, o que aproveita os processadores modernos de vários núcleos.

As listas de comandos normalmente são executadas uma vez. No entanto, uma lista de comandos poderá ser executada várias vezes se o aplicativo garantir que as execuções anteriores sejam concluídas antes de enviar novas execuções. Para obter mais informações sobre a sincronização da lista de comandos, consulte [Executando e sincronizando listas de comandos](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Agrupar itens de trabalho de GPU

Além das listas de comandos, o Direct3D 12 aproveita a funcionalidade presente em todos os hardwares atualmente adicionando um segundo nível de listas de comandos, que são chamados *de pacotes*. Para ajudar a distinguir esses dois tipos, as listas de comandos de primeiro nível podem ser conhecidas como *listas de comandos diretos.* A finalidade dos pacotes é permitir que os aplicativos a agrupam um pequeno número de comandos de API para execução repetida posterior em listas de comandos diretos. No momento da criação de um pacote, o driver executará o máximo de pré-processamento possível para tornar a execução posterior eficiente. Os pacotes podem ser executados de dentro de várias listas de comandos e várias vezes dentro da mesma lista de comandos.

O reuso de pacotes é um grande driver de maior eficiência com threads de CPU individuais. Como os pacotes são pré-processados e podem ser enviados várias vezes, há determinadas restrições sobre quais operações podem ser executadas em um pacote. Para obter mais informações, consulte [Criando e gravando listas de comandos e pacotes](recording-command-lists-and-bundles.md).

## <a name="gpu-work-submission"></a>Envio de trabalho de GPU

Para executar o trabalho na GPU, um aplicativo deve enviar explicitamente uma lista de comandos para uma fila de comandos associada ao dispositivo Direct3D. Uma lista de comandos diretos pode ser enviada para execução várias vezes, mas o aplicativo é responsável por garantir que a lista de comandos diretos tenha terminado de ser executada na GPU antes de encaminhá-la novamente. Os pacotes não têm restrições de uso simultâneo e podem ser executados várias vezes em várias listas de comandos, mas os pacotes não podem ser enviados diretamente a uma fila de comandos para execução.

Qualquer thread pode enviar uma lista de comandos para qualquer fila de comandos a qualquer momento e o runtime serializará automaticamente o envio da lista de comandos na fila de comandos preservando a ordem de envio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




