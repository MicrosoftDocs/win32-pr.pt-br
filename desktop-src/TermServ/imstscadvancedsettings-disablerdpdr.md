---
title: Propriedade IMsTscAdvancedSettings DisableRdpdr
description: Especifica se a impressora e o redirecionamento de área de transferência estão habilitados.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade DisableRdpdr
- Propriedade DisableRdpdr Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade DisableRdpdr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759938"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="80ea7-122">IMsTscAdvancedSettings: Propriedade isableRdpdr de:D</span><span class="sxs-lookup"><span data-stu-id="80ea7-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="80ea7-123">Especifica se a impressora e o redirecionamento de área de transferência estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="80ea7-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="80ea7-124">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="80ea7-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ea7-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="80ea7-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="80ea7-126">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="80ea7-126">Property value</span></span>

<span data-ttu-id="80ea7-127">Defina esse parâmetro como **true** para desabilitar o redirecionamento ou **falso** para habilitar o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="80ea7-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80ea7-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="80ea7-128">Error codes</span></span>

<span data-ttu-id="80ea7-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="80ea7-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="80ea7-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="80ea7-130">Remarks</span></span>

<span data-ttu-id="80ea7-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="80ea7-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80ea7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80ea7-132">Requirements</span></span>



| <span data-ttu-id="80ea7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="80ea7-133">Requirement</span></span> | <span data-ttu-id="80ea7-134">Valor</span><span class="sxs-lookup"><span data-stu-id="80ea7-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ea7-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80ea7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="80ea7-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80ea7-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="80ea7-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80ea7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="80ea7-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80ea7-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="80ea7-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="80ea7-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="80ea7-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80ea7-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="80ea7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="80ea7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80ea7-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80ea7-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="80ea7-143">IID</span><span class="sxs-lookup"><span data-stu-id="80ea7-143">IID</span></span><br/>                      | <span data-ttu-id="80ea7-144">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="80ea7-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80ea7-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="80ea7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ea7-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="80ea7-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="80ea7-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="80ea7-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="80ea7-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="80ea7-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="80ea7-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="80ea7-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="80ea7-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="80ea7-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="80ea7-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="80ea7-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="80ea7-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="80ea7-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="80ea7-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="80ea7-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="80ea7-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="80ea7-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





