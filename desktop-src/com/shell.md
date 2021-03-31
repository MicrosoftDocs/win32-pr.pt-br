---
title: Shell (COM)
description: Fornece informações de impressão do shell do Windows 3,1 e abertura de arquivo.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM chave do registro do Shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644111"
---
# <a name="shell-com"></a><span data-ttu-id="f5e8f-104">Shell (COM)</span><span class="sxs-lookup"><span data-stu-id="f5e8f-104">Shell (COM)</span></span>

<span data-ttu-id="f5e8f-105">Fornece informações de impressão do shell do Windows 3,1 e **abertura de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="f5e8f-105">Provides Windows 3.1 shell printing and **File Open** information.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f5e8f-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="f5e8f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a><span data-ttu-id="f5e8f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5e8f-107">Remarks</span></span>

<span data-ttu-id="f5e8f-108">Essas entradas devem fornecer o caminho e o nome do arquivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f5e8f-108">These entries should provide the path and file name of the application.</span></span>

 

 




