---
title: Comunicação Single-Threaded e multithread
description: Comunicação Single-Threaded e multithread
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292015"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Comunicação Single-Threaded e multithread

Um cliente ou servidor que dá suporte a Apartments de thread único e multi-threaded terá um apartamento multi-threaded, contendo todos os threads inicializados como de thread livre e um ou mais Apartments de thread único. Os ponteiros de interface devem ser empacotados entre Apartments, mas podem ser usados sem marshaling em um apartamento. As chamadas para objetos em um apartamento de thread único serão sincronizadas pelo COM. As chamadas para objetos no apartamento multi-threaded não serão sincronizadas pelo COM.

Todas as informações sobre Apartments de thread único se aplicam aos threads marcados como modelo de apartamento, e todas as informações em Apartments multithread se aplicam a todos os threads marcados como livres de threads. As regras de Threading Apartment se aplicam à comunicação entre apartamento, exigindo que os ponteiros de interface sejam empacotados entre Apartments com chamadas para [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) e [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), conforme descrito em [Apartments de thread único](single-threaded-apartments.md).

> [!Note]  
> Algumas considerações especiais se aplicam ao lidar com servidores em processo. Para obter mais informações, consulte [problemas de thread de servidor em processo](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando interfaces em Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Escolhendo o modelo de Threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartments multithread](multithreaded-apartments.md)
</dt> <dt>

[Problemas de Threading do servidor em processo](in-process-server-threading-issues.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Apartments de thread único](single-threaded-apartments.md)
</dt> </dl>

 

 




