---
title: Propriedade IMsRdpClientAdvancedSettings minInputSendInterval
description: Especifica o intervalo mínimo, em milissegundos, entre o envio de eventos do mouse.
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade minInputSendInterval
- Propriedade minInputSendInterval Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade minInputSendInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369440"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="1be24-120">Propriedade IMsRdpClientAdvancedSettings:: minInputSendInterval</span><span class="sxs-lookup"><span data-stu-id="1be24-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="1be24-121">Especifica o intervalo mínimo, em milissegundos, entre o envio de eventos do mouse.</span><span class="sxs-lookup"><span data-stu-id="1be24-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="1be24-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1be24-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1be24-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="1be24-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="1be24-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1be24-124">Property value</span></span>

<span data-ttu-id="1be24-125">O novo intervalo, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="1be24-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="1be24-126">O valor padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="1be24-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1be24-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1be24-127">Error codes</span></span>

<span data-ttu-id="1be24-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1be24-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1be24-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="1be24-129">Remarks</span></span>

<span data-ttu-id="1be24-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1be24-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1be24-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1be24-131">Requirements</span></span>



| <span data-ttu-id="1be24-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be24-132">Requirement</span></span> | <span data-ttu-id="1be24-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1be24-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be24-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be24-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1be24-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1be24-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="1be24-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be24-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1be24-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1be24-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="1be24-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1be24-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="1be24-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1be24-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1be24-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1be24-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1be24-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1be24-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1be24-142">IID</span><span class="sxs-lookup"><span data-stu-id="1be24-142">IID</span></span><br/>                      | <span data-ttu-id="1be24-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="1be24-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1be24-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be24-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be24-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1be24-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1be24-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1be24-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1be24-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1be24-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1be24-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1be24-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1be24-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1be24-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1be24-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1be24-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1be24-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1be24-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1be24-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="1be24-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





