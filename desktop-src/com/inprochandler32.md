---
title: InprocHandler32
description: InprocHandler32 especifica se um aplicativo usa um manipulador personalizado na chave HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID do Registro.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Chave do Registro InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405999"
---
# <a name="inprochandler32"></a><span data-ttu-id="5f5c2-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="5f5c2-104">InprocHandler32</span></span>

<span data-ttu-id="5f5c2-105">Especifica se um aplicativo usa um manipulador personalizado.</span><span class="sxs-lookup"><span data-stu-id="5f5c2-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5f5c2-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="5f5c2-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="5f5c2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f5c2-107">Remarks</span></span>

<span data-ttu-id="5f5c2-108">Esse é um **valor \_ REG SZ** que especifica o manipulador personalizado usado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f5c2-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="5f5c2-109">Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="5f5c2-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="5f5c2-110">Se um contêiner estiver pesquisando no Registro um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5f5c2-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f5c2-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f5c2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f5c2-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="5f5c2-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




