---
title: Propriedade IMsRdpClientAdvancedSettings singleConnectionTimeout
description: Especifica o período máximo de tempo, em segundos, que o controle de cliente espera por uma conexão com um endereço IP.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade singleConnectionTimeout
- Propriedade singleConnectionTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade singleConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369233"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="06916-120">Propriedade IMsRdpClientAdvancedSettings:: singleConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="06916-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="06916-121">Especifica o período máximo de tempo, em segundos, que o controle de cliente espera por uma conexão com um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="06916-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="06916-122">Durante a conexão, o controle pode tentar se conectar a vários endereços IP.</span><span class="sxs-lookup"><span data-stu-id="06916-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="06916-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="06916-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="06916-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="06916-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="06916-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="06916-125">Property value</span></span>

<span data-ttu-id="06916-126">O novo horário, em segundos.</span><span class="sxs-lookup"><span data-stu-id="06916-126">The new time, in seconds.</span></span> <span data-ttu-id="06916-127">O valor máximo é 600.</span><span class="sxs-lookup"><span data-stu-id="06916-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06916-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="06916-128">Error codes</span></span>

<span data-ttu-id="06916-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="06916-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="06916-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="06916-130">Remarks</span></span>

<span data-ttu-id="06916-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="06916-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06916-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06916-132">Requirements</span></span>



| <span data-ttu-id="06916-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="06916-133">Requirement</span></span> | <span data-ttu-id="06916-134">Valor</span><span class="sxs-lookup"><span data-stu-id="06916-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06916-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06916-135">Minimum supported client</span></span><br/> | <span data-ttu-id="06916-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06916-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="06916-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06916-137">Minimum supported server</span></span><br/> | <span data-ttu-id="06916-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06916-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="06916-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="06916-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="06916-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06916-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="06916-141">DLL</span><span class="sxs-lookup"><span data-stu-id="06916-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06916-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06916-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="06916-143">IID</span><span class="sxs-lookup"><span data-stu-id="06916-143">IID</span></span><br/>                      | <span data-ttu-id="06916-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="06916-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06916-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="06916-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06916-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="06916-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="06916-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="06916-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="06916-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="06916-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="06916-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="06916-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="06916-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="06916-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="06916-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="06916-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="06916-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="06916-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="06916-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="06916-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="06916-154">**overallConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="06916-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





