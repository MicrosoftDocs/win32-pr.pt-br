---
title: Propriedade IMsRdpClientAdvancedSettings ShadowBitmap
description: Especifica se os bitmaps de sombra devem ser usados.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ShadowBitmap
- Propriedade ShadowBitmap Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ShadowBitmap
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454651"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a><span data-ttu-id="484e6-120">Propriedade IMsRdpClientAdvancedSettings:: ShadowBitmap</span><span class="sxs-lookup"><span data-stu-id="484e6-120">IMsRdpClientAdvancedSettings::ShadowBitmap property</span></span>

<span data-ttu-id="484e6-121">\[Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="484e6-121">\[This property is not supported.</span></span> <span data-ttu-id="484e6-122">A partir do Windows Server 2008 e do Windows 7, as chamadas para **ShadowBitmap** sempre retornam **S \_ false**.\]</span><span class="sxs-lookup"><span data-stu-id="484e6-122">Starting with Windows Server 2008 and Windows 7, calls to **ShadowBitmap** always return **S\_FALSE**.\]</span></span>

<span data-ttu-id="484e6-123">Especifica se os bitmaps de sombra devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="484e6-123">Specifies if shadow bitmaps should be used.</span></span>

<span data-ttu-id="484e6-124">Os bitmaps de sombra são sempre desabilitados no modo de tela inteira, portanto, essa propriedade não tem nenhum efeito quando estiver no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="484e6-124">Shadow bitmaps are always disabled in full-screen mode, therefore this property has no effect when in full-screen mode.</span></span>

<span data-ttu-id="484e6-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="484e6-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="484e6-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="484e6-126">Syntax</span></span>


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="484e6-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="484e6-127">Property value</span></span>

<span data-ttu-id="484e6-128">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="484e6-128">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="484e6-129">A desabilitação desse recurso normalmente melhora o desempenho, mas pode resultar em artefatos ao pintar telas.</span><span class="sxs-lookup"><span data-stu-id="484e6-129">Disabling this feature typically improves performance but can result in artifacts when painting screens.</span></span>

## <a name="remarks"></a><span data-ttu-id="484e6-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="484e6-130">Remarks</span></span>

<span data-ttu-id="484e6-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="484e6-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="484e6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="484e6-132">Requirements</span></span>



| <span data-ttu-id="484e6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="484e6-133">Requirement</span></span> | <span data-ttu-id="484e6-134">Valor</span><span class="sxs-lookup"><span data-stu-id="484e6-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="484e6-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="484e6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="484e6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="484e6-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="484e6-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="484e6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="484e6-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="484e6-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="484e6-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="484e6-139">End of client support</span></span><br/>    | <span data-ttu-id="484e6-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="484e6-140">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="484e6-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="484e6-141">End of server support</span></span><br/>    | <span data-ttu-id="484e6-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="484e6-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="484e6-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="484e6-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="484e6-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="484e6-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="484e6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="484e6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="484e6-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="484e6-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="484e6-147">IID</span><span class="sxs-lookup"><span data-stu-id="484e6-147">IID</span></span><br/>                      | <span data-ttu-id="484e6-148">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="484e6-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="484e6-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="484e6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="484e6-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="484e6-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="484e6-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="484e6-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="484e6-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="484e6-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="484e6-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="484e6-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="484e6-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="484e6-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="484e6-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="484e6-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="484e6-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="484e6-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="484e6-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="484e6-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





