---
description: Membros do CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membros do CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766981"
---
# <a name="cmspcallmultigraph-members"></a>Membros do CMSPCallMultiGraph

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

Os blocos de espera armazenam as informações sobre a espera registrada no pool de threads. Ele inclui os identificadores de espera retornados pela chamada [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) e um ponteiro para a estrutura de contexto. Cada bloco na matriz é para um grafo em um dos objetos Stream. O deslocamento de um bloco nessa matriz é o mesmo que o deslocamento do fluxo que possui o grafo.

 

 
