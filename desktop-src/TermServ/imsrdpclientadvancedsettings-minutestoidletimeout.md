---
title: Propriedade IMsRdpClientAdvancedSettings MinutesToIdleTimeout
description: Especifica o período máximo de tempo, em minutos, que o cliente deve permanecer conectado sem a entrada do usuário. Se o tempo especificado decorrer, o controle chamará o método IMsTscAxEvents OnIdleTimeoutNotification.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade MinutesToIdleTimeout
- Propriedade MinutesToIdleTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade MinutesToIdleTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810443"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a><span data-ttu-id="39d4b-121">Propriedade IMsRdpClientAdvancedSettings:: MinutesToIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="39d4b-121">IMsRdpClientAdvancedSettings::MinutesToIdleTimeout property</span></span>

<span data-ttu-id="39d4b-122">Especifica o período máximo de tempo, em minutos, que o cliente deve permanecer conectado sem a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="39d4b-122">Specifies the maximum length of time, in minutes, that the client should remain connected without user input.</span></span> <span data-ttu-id="39d4b-123">Se o tempo especificado decorrer, o controle chamará o método [**IMsTscAxEvents:: OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="39d4b-123">If the specified time elapses, the control calls the [**IMsTscAxEvents::OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) method.</span></span>

<span data-ttu-id="39d4b-124">Você pode usar essa propriedade em uma situação em que você precisa desconectar uma sessão ociosa; por exemplo, em um ambiente de quiosque.</span><span class="sxs-lookup"><span data-stu-id="39d4b-124">You can use this property in a situation where you need to disconnect an idle session; for example, in a kiosk environment.</span></span>

<span data-ttu-id="39d4b-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="39d4b-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d4b-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d4b-126">Syntax</span></span>


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="39d4b-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="39d4b-127">Property value</span></span>

<span data-ttu-id="39d4b-128">A nova hora, em minutos.</span><span class="sxs-lookup"><span data-stu-id="39d4b-128">The new time, in minutes.</span></span> <span data-ttu-id="39d4b-129">O valor padrão é zero, que desabilita o recurso.</span><span class="sxs-lookup"><span data-stu-id="39d4b-129">The default value is zero, which disables the feature.</span></span> <span data-ttu-id="39d4b-130">O valor máximo é 240, que representa 4 horas.</span><span class="sxs-lookup"><span data-stu-id="39d4b-130">The maximum value is 240, which represents 4 hours.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39d4b-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="39d4b-131">Error codes</span></span>

<span data-ttu-id="39d4b-132">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="39d4b-132">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="39d4b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="39d4b-133">Remarks</span></span>

<span data-ttu-id="39d4b-134">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="39d4b-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39d4b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39d4b-135">Requirements</span></span>



| <span data-ttu-id="39d4b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d4b-136">Requirement</span></span> | <span data-ttu-id="39d4b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="39d4b-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d4b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39d4b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39d4b-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39d4b-139">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="39d4b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39d4b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39d4b-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39d4b-141">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="39d4b-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="39d4b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="39d4b-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d4b-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="39d4b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="39d4b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39d4b-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d4b-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="39d4b-146">IID</span><span class="sxs-lookup"><span data-stu-id="39d4b-146">IID</span></span><br/>                      | <span data-ttu-id="39d4b-147">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="39d4b-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39d4b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="39d4b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d4b-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="39d4b-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="39d4b-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="39d4b-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="39d4b-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="39d4b-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="39d4b-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="39d4b-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="39d4b-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="39d4b-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="39d4b-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="39d4b-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="39d4b-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="39d4b-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="39d4b-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="39d4b-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





