---
title: Exemplo de valores de registro
description: O exemplo a seguir mostra possíveis dados para alguns dos valores de registro do protocolo de autenticação.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104006956"
---
# <a name="registry-values-example"></a><span data-ttu-id="abbb8-103">Exemplo de valores de registro</span><span class="sxs-lookup"><span data-stu-id="abbb8-103">Registry Values Example</span></span>

<span data-ttu-id="abbb8-104">O exemplo a seguir mostra possíveis dados para alguns dos valores de registro do protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="abbb8-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="abbb8-105">Nome da Chave</span><span class="sxs-lookup"><span data-stu-id="abbb8-105">Key Name</span></span>            | <span data-ttu-id="abbb8-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="abbb8-106">Datatype</span></span>        | <span data-ttu-id="abbb8-107">Valor</span><span class="sxs-lookup"><span data-stu-id="abbb8-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="abbb8-108">Caminho</span><span class="sxs-lookup"><span data-stu-id="abbb8-108">Path</span></span>                | <span data-ttu-id="abbb8-109">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="abbb8-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="abbb8-110">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="abbb8-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="abbb8-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="abbb8-111">FriendlyName</span></span>        | <span data-ttu-id="abbb8-112">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="abbb8-112">REG\_SZ</span></span>         | <span data-ttu-id="abbb8-113">Protocolo EAP de exemplo</span><span class="sxs-lookup"><span data-stu-id="abbb8-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="abbb8-114">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="abbb8-114">ConfigUIPath</span></span>        | <span data-ttu-id="abbb8-115">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="abbb8-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="abbb8-116">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="abbb8-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="abbb8-117">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="abbb8-117">IdentityPath</span></span>        | <span data-ttu-id="abbb8-118">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="abbb8-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="abbb8-119">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="abbb8-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="abbb8-120">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="abbb8-120">InteractiveUIPath</span></span>   | <span data-ttu-id="abbb8-121">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="abbb8-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="abbb8-122">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="abbb8-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="abbb8-123">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="abbb8-123">RequireConfigUI</span></span>     | <span data-ttu-id="abbb8-124">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="abbb8-124">REG\_DWORD</span></span>      | <span data-ttu-id="abbb8-125">1</span><span class="sxs-lookup"><span data-stu-id="abbb8-125">1</span></span>                                      |
| <span data-ttu-id="abbb8-126">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="abbb8-126">ConfigCLSID</span></span>         | <span data-ttu-id="abbb8-127">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="abbb8-127">REG\_SZ</span></span>         | <span data-ttu-id="abbb8-128">{0000031A-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="abbb8-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="abbb8-129">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="abbb8-129">StandaloneSupported</span></span> | <span data-ttu-id="abbb8-130">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="abbb8-130">REG\_DWORD</span></span>      | <span data-ttu-id="abbb8-131">1</span><span class="sxs-lookup"><span data-stu-id="abbb8-131">1</span></span>                                      |



 

 

 




