---
title: Header do conjunto de propriedades
description: No início do fluxo do conjunto de propriedades está um header. Ele consiste em um indicador de ordem de byte, uma versão de formato, a versão do sistema operacional de origem, o CLSID (identificador de classe) e um campo reservado.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Estruturação estruturada do Armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662216"
---
# <a name="property-set-header"></a>Header do conjunto de propriedades

No início do fluxo do conjunto de propriedades está um header. Ele consiste em um indicador de ordem de byte, uma versão de formato, a versão do sistema operacional de origem, o CLSID (identificador de classe) e um campo reservado.

A pseudo-estrutura a seguir ilustra o header.

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




