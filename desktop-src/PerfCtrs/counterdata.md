---
description: A tabela CounterData contém uma linha para cada contador coletado em um determinado momento. Haverá um grande número dessas linhas.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Counterdata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b352b9ec6bde6e644d80e7556ac46211212b66b4d92601deedaecaa5dd07344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033986"
---
# <a name="counterdata"></a>Counterdata

A **tabela CounterData** contém uma linha para cada contador coletado em um determinado momento. Haverá um grande número dessas linhas.

A **tabela CounterData** define os seguintes campos:

-   **GUID:** GUID para esse conjunto de dados. Use essa chave para unir com a [**tabela DisplayToID.**](displaytoid.md)
-   **CounterID:** Identifica o contador. Use essa chave para unir com a [**tabela CounterDetails.**](counterdetails.md)
-   **RecordIndex:** O índice de exemplo para um identificador de contador específico e GUID de coleção. O valor aumenta para cada amostra sucessiva neste arquivo de log.
-   **CounterDateTime:** A hora em que a coleção foi iniciada, no horário UTC.
-   **CounterValue:** O valor formatado do contador. Esse valor pode ser zero para o primeiro registro se o contador exigir dois exemplos para calcular um valor exibivel.
-   **FirstValueA:** Combine esse valor de 32 bits com o valor **de FirstValueB** para criar o membro **FirstValue** do [**PDH \_ RAW \_ COUNTER.**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) **FirstValueA** contém os bits de ordem baixa.
-   **FirstValueB:** Combine esse valor de 32 bits com o valor **de FirstValueA** para criar o membro **FirstValue** do [**PDH \_ RAW \_ COUNTER.**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) **FirstValueB** contém os bits de ordem alta.
-   **SecondValueA:** Combine esse valor de 32 bits com o valor **de SecondValueB** para criar o membro **SecondValue** de [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA** contém os bits de ordem baixa.
-   **SecondValueB:** Combine esse valor de 32 bits com o valor **secondValueA** para criar o membro **SecondValue** de [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB** contém os bits de ordem alta.

Os **campos GUID,** **CounterID** e **RecordIndex** comem a chave primária para esta tabela.

 

 



