---
title: InprocHandler
description: InprocHandler especifica se um aplicativo usa um manipulador personalizado na HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID do Registro.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Chave do Registro InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404729"
---
# <a name="inprochandler"></a><span data-ttu-id="1556d-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="1556d-104">InprocHandler</span></span>

<span data-ttu-id="1556d-105">Especifica se um aplicativo usa um manipulador personalizado.</span><span class="sxs-lookup"><span data-stu-id="1556d-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1556d-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="1556d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="1556d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1556d-107">Remarks</span></span>

<span data-ttu-id="1556d-108">Esse é um **valor \_ REG SZ** que especifica o manipulador personalizado usado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1556d-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="1556d-109">Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="1556d-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="1556d-110">Se um contêiner estiver pesquisando no Registro um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1556d-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1556d-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1556d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1556d-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="1556d-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




