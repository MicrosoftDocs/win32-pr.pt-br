---
title: Propriedade IMsRdpClientAdvancedSettings RDPPort
description: Especifica a porta de conexão.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RDPPort
- Propriedade RDPPort Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RDPPort
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086387"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="71a70-120">Propriedade IMsRdpClientAdvancedSettings:: RDPPort</span><span class="sxs-lookup"><span data-stu-id="71a70-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="71a70-121">Especifica a porta de conexão.</span><span class="sxs-lookup"><span data-stu-id="71a70-121">Specifies the connection port.</span></span>

<span data-ttu-id="71a70-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="71a70-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a70-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="71a70-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="71a70-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="71a70-124">Property value</span></span>

<span data-ttu-id="71a70-125">A nova porta.</span><span class="sxs-lookup"><span data-stu-id="71a70-125">The new port.</span></span> <span data-ttu-id="71a70-126">O valor padrão é 3389.</span><span class="sxs-lookup"><span data-stu-id="71a70-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71a70-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="71a70-127">Error codes</span></span>

<span data-ttu-id="71a70-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="71a70-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="71a70-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="71a70-129">Remarks</span></span>

<span data-ttu-id="71a70-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="71a70-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71a70-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a70-131">Requirements</span></span>



| <span data-ttu-id="71a70-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a70-132">Requirement</span></span> | <span data-ttu-id="71a70-133">Valor</span><span class="sxs-lookup"><span data-stu-id="71a70-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a70-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a70-134">Minimum supported client</span></span><br/> | <span data-ttu-id="71a70-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71a70-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="71a70-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a70-136">Minimum supported server</span></span><br/> | <span data-ttu-id="71a70-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71a70-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="71a70-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="71a70-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="71a70-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a70-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="71a70-140">DLL</span><span class="sxs-lookup"><span data-stu-id="71a70-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71a70-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a70-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="71a70-142">IID</span><span class="sxs-lookup"><span data-stu-id="71a70-142">IID</span></span><br/>                      | <span data-ttu-id="71a70-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="71a70-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71a70-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="71a70-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a70-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="71a70-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="71a70-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="71a70-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="71a70-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="71a70-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="71a70-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="71a70-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="71a70-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="71a70-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="71a70-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="71a70-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="71a70-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="71a70-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="71a70-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="71a70-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





