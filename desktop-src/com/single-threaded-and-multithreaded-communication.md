---
title: Comunicação Single-Threaded e multithread
description: Comunicação Single-Threaded e multithread
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1096ff2cd5916bf16b00a746c2e6de6ce22008258c6e200c2858c0430cb3f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129828"
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

 

 




