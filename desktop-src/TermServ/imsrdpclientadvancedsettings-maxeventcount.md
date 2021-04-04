---
title: Propriedade IMsRdpClientAdvancedSettings maxEventCount
description: Não há suporte a esta propriedade. | Propriedade IMsRdpClientAdvancedSettings maxEventCount
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade maxEventCount
- Propriedade maxEventCount Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade maxEventCount
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb305d4a81b3c4dd9eb53dceab5a4e685c57c060
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837768"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a><span data-ttu-id="309de-121">Propriedade IMsRdpClientAdvancedSettings:: maxEventCount</span><span class="sxs-lookup"><span data-stu-id="309de-121">IMsRdpClientAdvancedSettings::maxEventCount property</span></span>

<span data-ttu-id="309de-122">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="309de-122">This property is not supported.</span></span>

<span data-ttu-id="309de-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="309de-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="309de-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="309de-124">Syntax</span></span>


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a><span data-ttu-id="309de-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="309de-125">Property value</span></span>

<span data-ttu-id="309de-126">A nova contagem de eventos.</span><span class="sxs-lookup"><span data-stu-id="309de-126">The new event count.</span></span> <span data-ttu-id="309de-127">O padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="309de-127">The default is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="309de-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="309de-128">Error codes</span></span>

<span data-ttu-id="309de-129">Retorna **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="309de-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="309de-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="309de-130">Remarks</span></span>

<span data-ttu-id="309de-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="309de-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="309de-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="309de-132">Requirements</span></span>



| <span data-ttu-id="309de-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="309de-133">Requirement</span></span> | <span data-ttu-id="309de-134">Valor</span><span class="sxs-lookup"><span data-stu-id="309de-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="309de-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="309de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="309de-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="309de-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="309de-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="309de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="309de-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="309de-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="309de-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="309de-139">End of client support</span></span><br/>    | <span data-ttu-id="309de-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="309de-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="309de-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="309de-141">End of server support</span></span><br/>    | <span data-ttu-id="309de-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="309de-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="309de-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="309de-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="309de-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="309de-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="309de-145">DLL</span><span class="sxs-lookup"><span data-stu-id="309de-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="309de-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="309de-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="309de-147">IID</span><span class="sxs-lookup"><span data-stu-id="309de-147">IID</span></span><br/>                      | <span data-ttu-id="309de-148">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="309de-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="309de-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="309de-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="309de-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="309de-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="309de-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="309de-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="309de-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="309de-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="309de-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="309de-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="309de-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="309de-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="309de-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="309de-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="309de-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="309de-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="309de-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="309de-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





