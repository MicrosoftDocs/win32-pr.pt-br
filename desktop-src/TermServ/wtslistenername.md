---
title: WTSLISTENERNAME (WtsApi32. h)
description: Representa o nome de um ouvinte de Serviços de Área de Trabalho Remota em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369763"
---
# <a name="wtslistenername"></a><span data-ttu-id="cd920-109">WTSLISTENERNAME</span><span class="sxs-lookup"><span data-stu-id="cd920-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="cd920-110">Representa o nome de um ouvinte de Serviços de Área de Trabalho Remota em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="cd920-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="cd920-111">**WTSLISTENERNAMEW**</span><span class="sxs-lookup"><span data-stu-id="cd920-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="cd920-112">O nome Unicode do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="cd920-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="cd920-113">**WTSLISTENERNAMEA**</span><span class="sxs-lookup"><span data-stu-id="cd920-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="cd920-114">Um ponteiro para o nome ANSI do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="cd920-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="cd920-115">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="cd920-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="cd920-116">O nome do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="cd920-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="cd920-117">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="cd920-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="cd920-118">Um ponteiro para o nome do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="cd920-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="cd920-119">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="cd920-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="cd920-120">O nome do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="cd920-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="cd920-121">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="cd920-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="cd920-122">Um ponteiro para o nome do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="cd920-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd920-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd920-123">Requirements</span></span>



| <span data-ttu-id="cd920-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd920-124">Requirement</span></span> | <span data-ttu-id="cd920-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cd920-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd920-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd920-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cd920-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd920-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="cd920-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd920-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cd920-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd920-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="cd920-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd920-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd920-131"><dt>WtsApi32. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd920-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 





