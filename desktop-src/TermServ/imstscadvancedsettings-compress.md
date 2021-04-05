---
title: Propriedade de compactação IMsTscAdvancedSettings
description: Especifica se a compactação está habilitada.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de compactação
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade compress
- Serviços de Área de Trabalho Remota da propriedade compress, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade compress
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918651"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="26d6d-122">Propriedade IMsTscAdvancedSettings:: compress</span><span class="sxs-lookup"><span data-stu-id="26d6d-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="26d6d-123">Especifica se a compactação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="26d6d-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="26d6d-124">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="26d6d-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d6d-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="26d6d-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="26d6d-126">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="26d6d-126">Property value</span></span>

<span data-ttu-id="26d6d-127">Defina esse parâmetro como 0 para desabilitar a compactação ou um valor diferente de zero para habilitar a compactação.</span><span class="sxs-lookup"><span data-stu-id="26d6d-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26d6d-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="26d6d-128">Error codes</span></span>

<span data-ttu-id="26d6d-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="26d6d-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d6d-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="26d6d-130">Remarks</span></span>

<span data-ttu-id="26d6d-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="26d6d-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26d6d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d6d-132">Requirements</span></span>



| <span data-ttu-id="26d6d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d6d-133">Requirement</span></span> | <span data-ttu-id="26d6d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="26d6d-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d6d-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d6d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="26d6d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26d6d-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="26d6d-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d6d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="26d6d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26d6d-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="26d6d-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="26d6d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="26d6d-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d6d-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="26d6d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="26d6d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d6d-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d6d-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="26d6d-143">IID</span><span class="sxs-lookup"><span data-stu-id="26d6d-143">IID</span></span><br/>                      | <span data-ttu-id="26d6d-144">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="26d6d-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26d6d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="26d6d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d6d-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="26d6d-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="26d6d-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="26d6d-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="26d6d-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="26d6d-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="26d6d-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="26d6d-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="26d6d-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="26d6d-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="26d6d-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="26d6d-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="26d6d-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="26d6d-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="26d6d-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="26d6d-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="26d6d-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="26d6d-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





