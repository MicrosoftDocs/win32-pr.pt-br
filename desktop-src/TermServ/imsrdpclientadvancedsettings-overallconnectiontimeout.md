---
title: Propriedade IMsRdpClientAdvancedSettings overallConnectionTimeout
description: Especifica o período total de tempo, em segundos, que o controle de cliente aguarda até que uma conexão seja concluída.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade overallConnectionTimeout
- Propriedade overallConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade overallConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753329"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a><span data-ttu-id="de5d9-120">Propriedade IMsRdpClientAdvancedSettings:: overallConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="de5d9-120">IMsRdpClientAdvancedSettings::overallConnectionTimeout property</span></span>

<span data-ttu-id="de5d9-121">Especifica o período total de tempo, em segundos, que o controle de cliente aguarda até que uma conexão seja concluída.</span><span class="sxs-lookup"><span data-stu-id="de5d9-121">Specifies the total length of time, in seconds, that the client control waits for a connection to complete.</span></span>

<span data-ttu-id="de5d9-122">Se o tempo especificado tiver decorrido antes de a conexão ser concluída, o controle desconectará e chamará o método [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) .</span><span class="sxs-lookup"><span data-stu-id="de5d9-122">If the specified time elapses before connection completes, the control disconnects and calls the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) method.</span></span>

<span data-ttu-id="de5d9-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="de5d9-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5d9-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="de5d9-124">Syntax</span></span>


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="de5d9-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="de5d9-125">Property value</span></span>

<span data-ttu-id="de5d9-126">O novo horário, em segundos.</span><span class="sxs-lookup"><span data-stu-id="de5d9-126">The new time, in seconds.</span></span> <span data-ttu-id="de5d9-127">O valor máximo é 600, que representa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="de5d9-127">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de5d9-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="de5d9-128">Error codes</span></span>

<span data-ttu-id="de5d9-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="de5d9-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5d9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="de5d9-130">Remarks</span></span>

<span data-ttu-id="de5d9-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="de5d9-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de5d9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de5d9-132">Requirements</span></span>



| <span data-ttu-id="de5d9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5d9-133">Requirement</span></span> | <span data-ttu-id="de5d9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="de5d9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5d9-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de5d9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="de5d9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de5d9-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="de5d9-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de5d9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="de5d9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de5d9-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="de5d9-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de5d9-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="de5d9-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de5d9-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="de5d9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="de5d9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de5d9-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de5d9-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="de5d9-143">IID</span><span class="sxs-lookup"><span data-stu-id="de5d9-143">IID</span></span><br/>                      | <span data-ttu-id="de5d9-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="de5d9-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de5d9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="de5d9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5d9-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="de5d9-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="de5d9-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="de5d9-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="de5d9-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="de5d9-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="de5d9-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="de5d9-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="de5d9-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="de5d9-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="de5d9-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="de5d9-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="de5d9-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="de5d9-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="de5d9-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="de5d9-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="de5d9-154">**singleConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="de5d9-154">**singleConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





