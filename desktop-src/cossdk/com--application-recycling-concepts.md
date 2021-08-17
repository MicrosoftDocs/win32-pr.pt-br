---
description: A reciclagem de aplicativos pode aumentar significativamente a estabilidade geral de seus aplicativos COM+, oferecendo uma correção rápida para problemas conhecidos e ajudando a proteger contra os inesperados.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: Conceitos de reciclagem de aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a635487427fce3f17203f11426261996348a5e4057ab8bceebcae552d51bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129258"
---
# <a name="com-application-recycling-concepts"></a>Conceitos de reciclagem de aplicativos COM+

A reciclagem de aplicativos pode aumentar significativamente a estabilidade geral de seus aplicativos COM+, oferecendo uma correção rápida para problemas conhecidos e ajudando a proteger contra os inesperados. Por exemplo, o desempenho do aplicativo pode ser degradado ao longo do tempo devido a problemas como vazamentos de memória, uso de recursos não pode ser escalado e falha de processo. O COM+ fornece reciclagem de aplicativos como uma solução para esses problemas. Você pode usar a reciclagem de aplicativos para desligar automaticamente um processo e reiniciá-lo, reinicializando assim um processo com falha e realocando a memória que ele usa.

A reciclagem de aplicativo funciona criando uma duplicata do processo Dllhost associado a um aplicativo. Esse processo Dllhost duplicado serviços todas as solicitações de objeto futuras, o que deixa o Dllhost antigo para concluir a manutenção das solicitações de objeto restantes. O processo de Dllhost antigo é desligado quando detecta a liberação de todas as referências externas a objetos no processo ou quando o valor de tempo de expiração é atingido. Por meio desse comportamento, a reciclagem de aplicativos garante que um aplicativo cliente não experimente uma interrupção de serviço.

> [!Note]  
> Você não pode reciclar um aplicativo COM+ que foi configurado para ser executado como um Windows serviço. Além disso, os aplicativos de biblioteca têm as propriedades de reciclagem e pooling de seu processo de host.

 

Você pode configurar a reciclagem de aplicativos administrativamente, usando a ferramenta administrativa serviços de componentes ou programaticamente, por meio do SDK Administrativo do COM+. Você pode reciclar processos com base em vários critérios, determinados pelas seguintes propriedades de um [**objeto COMAdminCatalogObject**](comadmincatalogobject.md) na coleção [**Applications:**](applications.md)

-   **RecycleLifetimeLimit.** O número máximo de minutos que um processo pode executar antes de ser reciclado. O intervalo válido é de 0 a 30.240 minutos (21 dias). O número padrão de minutos é 0, o que indica que o processo não será reciclado de atingir um limite de tempo de vida.
-   **RecycleMemoryLimit.** A quantidade máxima de uso de memória do processo (em quilobytes) antes de reciclar o processo. Se o uso da memória do processo exceder o número especificado por mais de um minuto, o processo será reciclado. O intervalo válido é de 0 a 1.048.576 KB. A quantidade padrão de uso de memória é 0 KB, o que indica que o processo não será reciclado ao atingir um limite de memória.
-   **RecycleCallLimit.** O número máximo de chamadas que os objetos de aplicativo podem aceitar antes de reciclar o processo. O intervalo válido é de 0 a 1.048.576 chamadas. O número padrão de chamadas é 0, o que indica que o processo não será reciclado ao atingir um limite de chamada.
-   **RecycleActivationLimit.** O número máximo de ativações de objeto de aplicativo a aceitar antes de reciclar o processo. O intervalo válido é de 0 a 1.048.576 ativações. O número padrão de ativações é 0, o que indica que o processo não será reciclado ao atingir um limite de ativação.

Além disso, a propriedade RecycleExpirationTimeout do objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) é usada para forçar o desligamento de um processo reciclado. Indica o número de minutos a aguardar a liberação de todas as referências externas a objetos no processo reciclado antes de desligar o processo à força. O intervalo válido é de 1 a 1440 minutos (24 horas) e o tempo de expiração padrão é de 15 minutos. Esse valor é usado somente quando já está determinado que um processo será reciclado com base nos outros critérios.

Você pode selecionar mais de um critério para reciclar um aplicativo. O COM+ recicla o aplicativo depois que o primeiro do conjunto de critérios é atendido. Você pode definir o valor de tempo de expiração para determinar por quanto tempo um processo de Dllhost antigo pode gastar concluindo as solicitações de serviço restantes antes de ser desligado à força.

A [**coleção ApplicationInstances**](applicationinstances.md) fornece a propriedade HasRecycled, que fornece uma maneira de determinar se o aplicativo já foi reciclado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de reciclagem de aplicativos COM+](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



