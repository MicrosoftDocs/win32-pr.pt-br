---
description: Devido à superfície de DLLs vinculadas estaticamente, você deve evitar o uso de MFC (MFCs) para escrever um especialista.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Usando MFC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362925"
---
# <a name="using-microsoft-foundation-classes"></a>Usando MFC

Devido à superfície de DLLs vinculadas estaticamente, você deve evitar o uso de MFC (MFCs) para escrever um especialista. No entanto, se você usar o MFC, verifique o acesso a qualquer um dos recursos de DLL do MFC, incluindo o código a seguir imediatamente após a entrada:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



