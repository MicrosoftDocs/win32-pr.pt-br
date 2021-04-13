---
title: Propriedade IMsRdpClientAdvancedSettings keepAliveInterval
description: Especifica um intervalo, em milissegundos, no qual o cliente envia mensagens Keep-Alive para o servidor.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade keepAliveInterval
- Propriedade keepAliveInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369442"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="ece07-120">Propriedade IMsRdpClientAdvancedSettings:: keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="ece07-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="ece07-121">Especifica um intervalo, em milissegundos, no qual o cliente envia mensagens Keep-Alive para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ece07-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="ece07-122">Uma configuração de política de grupo que especifica se as conexões de cliente persistentes com o servidor são permitidas podem substituir essa configuração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ece07-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="ece07-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ece07-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece07-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ece07-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="ece07-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ece07-125">Property value</span></span>

<span data-ttu-id="ece07-126">O novo intervalo, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ece07-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="ece07-127">O valor padrão da propriedade é zero, o que desabilita as mensagens Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="ece07-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="ece07-128">O valor mínimo válido dessa propriedade é 10.000, que representa 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="ece07-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ece07-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ece07-129">Error codes</span></span>

<span data-ttu-id="ece07-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ece07-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece07-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece07-131">Remarks</span></span>

<span data-ttu-id="ece07-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ece07-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ece07-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece07-133">Requirements</span></span>



| <span data-ttu-id="ece07-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece07-134">Requirement</span></span> | <span data-ttu-id="ece07-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ece07-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece07-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece07-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ece07-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ece07-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ece07-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece07-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ece07-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ece07-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ece07-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ece07-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ece07-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece07-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ece07-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ece07-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece07-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece07-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ece07-144">IID</span><span class="sxs-lookup"><span data-stu-id="ece07-144">IID</span></span><br/>                      | <span data-ttu-id="ece07-145">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ece07-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ece07-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="ece07-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece07-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ece07-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ece07-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ece07-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ece07-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ece07-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ece07-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ece07-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ece07-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ece07-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ece07-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ece07-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ece07-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ece07-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ece07-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ece07-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





