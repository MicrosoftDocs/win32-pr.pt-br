---
description: Devido à superfície de DLLs vinculadas estaticamente, você deve evitar o uso de MFC (MFCs) para escrever um especialista.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Usando MFC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662526"
---
# <a name="using-microsoft-foundation-classes"></a><span data-ttu-id="2c474-103">Usando MFC</span><span class="sxs-lookup"><span data-stu-id="2c474-103">Using Microsoft Foundation Classes</span></span>

<span data-ttu-id="2c474-104">Devido à superfície de DLLs vinculadas estaticamente, você deve evitar o uso de MFC (MFCs) para escrever um especialista.</span><span class="sxs-lookup"><span data-stu-id="2c474-104">Because of the footprint of statically linked DLLs, you should avoid using Microsoft Foundation Classes (MFCs) to write an expert.</span></span> <span data-ttu-id="2c474-105">No entanto, se você usar o MFC, verifique o acesso a qualquer um dos recursos de DLL do MFC, incluindo o código a seguir imediatamente após a entrada:</span><span class="sxs-lookup"><span data-stu-id="2c474-105">However, if you use the MFC, ensure access to any of the MFC DLL resources by including the following code immediately upon entry:</span></span>

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



