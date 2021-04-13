---
title: Propriedade IMsRdpClient6 AdvancedSettings7
description: Recupera a interface IMsRdpClientAdvancedSettings6.
ms.assetid: 64b05c66-ac6a-4190-9df8-4a88dbc46c3f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings7
- Propriedade AdvancedSettings7 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings7
- Propriedade AdvancedSettings7 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings7
- Propriedade AdvancedSettings7 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings7
- Propriedade AdvancedSettings7 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings7
- Propriedade AdvancedSettings7 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings7
- Propriedade AdvancedSettings7 Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade AdvancedSettings7
topic_type:
- apiref
api_name:
- IMsRdpClient6.AdvancedSettings7
- IMsRdpClient6.get_AdvancedSettings7
- IMsRdpClient7.AdvancedSettings7
- IMsRdpClient7.get_AdvancedSettings7
- IMsRdpClient8.AdvancedSettings7
- IMsRdpClient8.get_AdvancedSettings7
- IMsRdpClient9.AdvancedSettings7
- IMsRdpClient9.get_AdvancedSettings7
- IMsRdpClient10.AdvancedSettings7
- IMsRdpClient10.get_AdvancedSettings7
- MsRdpClient6.AdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51d364c14be3311272455e040d55f277f3fb136
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369383"
---
# <a name="imsrdpclient6advancedsettings7-property"></a><span data-ttu-id="db890-116">Propriedade IMsRdpClient6:: AdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="db890-116">IMsRdpClient6::AdvancedSettings7 property</span></span>

<span data-ttu-id="db890-117">Recupera a interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="db890-117">Retrieves the [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="db890-118">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="db890-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db890-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db890-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings7(
  [out] IMsRdpClientAdvancedSettings6 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="db890-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="db890-120">Property value</span></span>

<span data-ttu-id="db890-121">Um ponteiro de interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) .</span><span class="sxs-lookup"><span data-stu-id="db890-121">An [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="db890-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db890-122">Requirements</span></span>



| <span data-ttu-id="db890-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="db890-123">Requirement</span></span> | <span data-ttu-id="db890-124">Valor</span><span class="sxs-lookup"><span data-stu-id="db890-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db890-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db890-125">Minimum supported client</span></span><br/> | <span data-ttu-id="db890-126">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="db890-126">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="db890-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db890-127">Minimum supported server</span></span><br/> | <span data-ttu-id="db890-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db890-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="db890-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="db890-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="db890-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db890-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="db890-131">DLL</span><span class="sxs-lookup"><span data-stu-id="db890-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db890-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db890-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="db890-133">IID</span><span class="sxs-lookup"><span data-stu-id="db890-133">IID</span></span><br/>                      | <span data-ttu-id="db890-134">IID \_ IMsRdpClient6 é definido como d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="db890-134">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="db890-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="db890-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db890-136">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="db890-136">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="db890-137">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="db890-137">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="db890-138">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="db890-138">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="db890-139">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="db890-139">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="db890-140">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="db890-140">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





