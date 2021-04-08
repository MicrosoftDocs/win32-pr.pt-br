---
description: Você pode usar as funções a seguir para trabalhar com dados de desempenho no Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Funções de contadores de desempenho para Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828381"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Funções de contadores de desempenho para Visual Basic

> [!IMPORTANT]
> As funções descritas neste tópico podem ser alteradas ou não disponíveis no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Você pode usar as funções a seguir para trabalhar com dados de desempenho no Visual Basic.

- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhVbAddCounter**](pdhvbaddcounter.md)
- [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
- [**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
- [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
- [**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
- [**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
- [**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
- [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
- [**PdhVbOpenLog**](pdhvbopenlog.md)
- [**PdhVbOpenQuery**](pdhvbopenquery.md)
- [**PdhVbUpdateLog**](pdhvbupdatelog.md)

> [!NOTE]
> As `PdhVb***` funções funcionam em uma sessão por processo e não são thread-safe. Essas funções só devem ser usadas de aplicativos simples de thread único.
