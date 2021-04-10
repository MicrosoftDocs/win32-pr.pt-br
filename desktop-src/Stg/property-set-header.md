---
title: Cabeçalho do conjunto de propriedades
description: No início do fluxo do conjunto de propriedades está um cabeçalho. Ele consiste em um indicador de ordem de byte, uma versão de formato, a versão do sistema operacional de origem, o identificador de classe (CLSID) e um campo reservado.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Armazenamento estruturado do cabeçalho do conjunto de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292871"
---
# <a name="property-set-header"></a><span data-ttu-id="1b6c9-105">Cabeçalho do conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="1b6c9-105">Property Set Header</span></span>

<span data-ttu-id="1b6c9-106">No início do fluxo do conjunto de propriedades está um cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-106">At the beginning of the property set stream is a header.</span></span> <span data-ttu-id="1b6c9-107">Ele consiste em um indicador de ordem de byte, uma versão de formato, a versão do sistema operacional de origem, o identificador de classe (CLSID) e um campo reservado.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-107">It consists of a byte-order indicator, a format version, the originating operating system version, the class identifier (CLSID), and a reserved field.</span></span>

<span data-ttu-id="1b6c9-108">A pseudo estrutura a seguir ilustra o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1b6c9-108">The following pseudo-structure illustrates the header.</span></span>

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

 

 




