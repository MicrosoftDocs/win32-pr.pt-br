---
title: Problemas com vários threads
description: Problemas com vários threads
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918526"
---
# <a name="multi-threaded-issues"></a>Problemas com vários threads

O OLE dá suporte a aplicativos multithread, permitindo que os aplicativos façam chamadas OLE de vários threads. Esse suporte multithread é chamado de modelo apartment, é importante que todos os componentes OLE que usam vários threads sigam esse modelo. O modelo apartment requer que os ponteiros de interface sejam marshalados (usando [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) quando passados entre threads.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processos, threads e apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 




