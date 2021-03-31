---
description: Definir a parte ETYPE ou SAP do filtro de captura é a primeira etapa no processo de criação do filtro de captura.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Configurando o filtro ETYPE ou SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920993"
---
# <a name="setting-the-etype-or-sap-filter"></a>Configurando o filtro ETYPE ou SAP

Definir a parte ETYPE ou SAP do filtro de captura é a primeira etapa no processo de criação do filtro de captura.

No exemplo a seguir, o filtro de captura está definido para recuperar somente o tráfego IPX:


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



Os valores SAP e ETYPE geralmente estão disponíveis em RFCs. Os valores SAP e ETYPE podem estar em uma matriz.

 

 



