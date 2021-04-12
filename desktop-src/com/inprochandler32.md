---
title: InprocHandler32
description: Especifica se um aplicativo usa um manipulador personalizado.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32 de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363774"
---
# <a name="inprochandler32"></a><span data-ttu-id="187e5-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="187e5-104">InprocHandler32</span></span>

<span data-ttu-id="187e5-105">Especifica se um aplicativo usa um manipulador personalizado.</span><span class="sxs-lookup"><span data-stu-id="187e5-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="187e5-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="187e5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="187e5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="187e5-107">Remarks</span></span>

<span data-ttu-id="187e5-108">Este é um valor de **\_ sz de reg** que especifica o manipulador personalizado usado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="187e5-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="187e5-109">Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="187e5-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="187e5-110">Se um contêiner estiver pesquisando o registro em busca de um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="187e5-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="187e5-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="187e5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="187e5-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="187e5-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




