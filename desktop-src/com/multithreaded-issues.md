---
title: Problemas multi-threaded
description: Problemas multi-threaded
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364512"
---
# <a name="multi-threaded-issues"></a>Problemas multi-threaded

O OLE fornece suporte para aplicativos multissegmentados, permitindo que os aplicativos façam chamadas OLE de vários threads. Esse suporte multithread é chamado de modelo de apartamento, é importante que todos os componentes OLE que usam vários threads sigam esse modelo. O modelo de apartamento requer que os ponteiros de interface sejam empacotados (usando [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) quando passados entre threads.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 




