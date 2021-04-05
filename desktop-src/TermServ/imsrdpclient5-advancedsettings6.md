---
title: Propriedade IMsRdpClient5 AdvancedSettings6
description: Recupera a interface IMsRdpClientAdvancedSettings5.
ms.assetid: b6a4efcf-87c3-438c-b6de-8a497ee5939d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings6
- Propriedade AdvancedSettings6 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings6
- Propriedade AdvancedSettings6 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings6
- Propriedade AdvancedSettings6 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings6
- Propriedade AdvancedSettings6 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings6
- Propriedade AdvancedSettings6 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings6
- Propriedade AdvancedSettings6 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings6
topic_type:
- apiref
api_name:
- IMsRdpClient5.AdvancedSettings6
- IMsRdpClient5.get_AdvancedSettings6
- IMsRdpClient6.AdvancedSettings6
- IMsRdpClient6.get_AdvancedSettings6
- IMsRdpClient7.AdvancedSettings6
- IMsRdpClient7.get_AdvancedSettings6
- IMsRdpClient8.AdvancedSettings6
- IMsRdpClient8.get_AdvancedSettings6
- IMsRdpClient9.AdvancedSettings6
- IMsRdpClient9.get_AdvancedSettings6
- IMsRdpClient10.AdvancedSettings6
- IMsRdpClient10.get_AdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b93d2395ec7e673e50023867f4602eea5c2d9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824777"
---
# <a name="imsrdpclient5advancedsettings6-property"></a><span data-ttu-id="ad00d-116">Propriedade IMsRdpClient5:: AdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="ad00d-116">IMsRdpClient5::AdvancedSettings6 property</span></span>

<span data-ttu-id="ad00d-117">Recupera a interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="ad00d-117">Retrieves the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="ad00d-118">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ad00d-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad00d-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad00d-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings6(
  [out] IMsRdpClientAdvancedSettings5 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ad00d-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ad00d-120">Property value</span></span>

<span data-ttu-id="ad00d-121">Um ponteiro de interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ad00d-121">An [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad00d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad00d-122">Requirements</span></span>



| <span data-ttu-id="ad00d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad00d-123">Requirement</span></span> | <span data-ttu-id="ad00d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ad00d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad00d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad00d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad00d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad00d-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ad00d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad00d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad00d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad00d-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ad00d-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ad00d-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad00d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad00d-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad00d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ad00d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad00d-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad00d-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad00d-133">IID</span><span class="sxs-lookup"><span data-stu-id="ad00d-133">IID</span></span><br/>                      | <span data-ttu-id="ad00d-134">IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="ad00d-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ad00d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad00d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad00d-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ad00d-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ad00d-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ad00d-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ad00d-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ad00d-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ad00d-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ad00d-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ad00d-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ad00d-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ad00d-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ad00d-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





