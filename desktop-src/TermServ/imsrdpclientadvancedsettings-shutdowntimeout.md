---
title: Propriedade IMsRdpClientAdvancedSettings shutdownTimeout
description: Especifica o período de tempo, em segundos, para aguardar até que o servidor responda a uma solicitação de desconexão.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade shutdownTimeout
- Propriedade shutdownTimeout Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade shutdownTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369234"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a><span data-ttu-id="444d9-120">Propriedade IMsRdpClientAdvancedSettings:: shutdownTimeout</span><span class="sxs-lookup"><span data-stu-id="444d9-120">IMsRdpClientAdvancedSettings::shutdownTimeout property</span></span>

<span data-ttu-id="444d9-121">Especifica o período de tempo, em segundos, para aguardar até que o servidor responda a uma solicitação de desconexão.</span><span class="sxs-lookup"><span data-stu-id="444d9-121">Specifies the length of time, in seconds, to wait for the server to respond to a disconnection request.</span></span>

<span data-ttu-id="444d9-122">Se o servidor não responder dentro do tempo especificado, o controle de cliente será desconectado.</span><span class="sxs-lookup"><span data-stu-id="444d9-122">If the server does not reply within the specified time, the client control disconnects.</span></span>

<span data-ttu-id="444d9-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="444d9-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="444d9-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="444d9-124">Syntax</span></span>


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="444d9-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="444d9-125">Property value</span></span>

<span data-ttu-id="444d9-126">O novo horário, em segundos.</span><span class="sxs-lookup"><span data-stu-id="444d9-126">The new time, in seconds.</span></span> <span data-ttu-id="444d9-127">O valor padrão da propriedade é 10.</span><span class="sxs-lookup"><span data-stu-id="444d9-127">The default value of the property is 10.</span></span> <span data-ttu-id="444d9-128">O valor máximo é 600, que representa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="444d9-128">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="444d9-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="444d9-129">Error codes</span></span>

<span data-ttu-id="444d9-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="444d9-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="444d9-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="444d9-131">Remarks</span></span>

<span data-ttu-id="444d9-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="444d9-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="444d9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="444d9-133">Requirements</span></span>



| <span data-ttu-id="444d9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="444d9-134">Requirement</span></span> | <span data-ttu-id="444d9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="444d9-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="444d9-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="444d9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="444d9-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="444d9-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="444d9-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="444d9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="444d9-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="444d9-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="444d9-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="444d9-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="444d9-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="444d9-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="444d9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="444d9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="444d9-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="444d9-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="444d9-144">IID</span><span class="sxs-lookup"><span data-stu-id="444d9-144">IID</span></span><br/>                      | <span data-ttu-id="444d9-145">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="444d9-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="444d9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="444d9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444d9-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="444d9-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="444d9-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="444d9-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="444d9-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="444d9-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="444d9-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="444d9-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="444d9-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="444d9-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="444d9-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="444d9-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="444d9-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="444d9-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="444d9-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="444d9-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





