---
description: Definir a parte Etype ou SAP do filtro de captura é a primeira etapa no processo de criação do filtro de captura.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Definindo o filtro Etype ou SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363161"
---
# <a name="setting-the-etype-or-sap-filter"></a>Definindo o filtro Etype ou SAP

Definir a parte Etype ou SAP do filtro de captura é a primeira etapa no processo de criação do filtro de captura.

No exemplo a seguir, o filtro de captura é definido para recuperar apenas o tráfego IPX:


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



Os valores SAP e Etype geralmente estão disponíveis em RFCs. Os valores SAP e Etype podem estar em uma matriz.

 

 



