---
title: Propriedade IMsTscAdvancedSettings allowBackgroundInput
description: Especifica se o modo de entrada em segundo plano está habilitado.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade allowBackgroundInput
- Propriedade allowBackgroundInput Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade allowBackgroundInput
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369910"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a><span data-ttu-id="fa2cd-122">Propriedade IMsTscAdvancedSettings:: allowBackgroundInput</span><span class="sxs-lookup"><span data-stu-id="fa2cd-122">IMsTscAdvancedSettings::allowBackgroundInput property</span></span>

<span data-ttu-id="fa2cd-123">Especifica se o modo de entrada em segundo plano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fa2cd-123">Specifies whether background input mode is enabled.</span></span> <span data-ttu-id="fa2cd-124">Quando a entrada em segundo plano estiver habilitada, o cliente poderá aceitar a entrada quando o cliente não tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="fa2cd-124">When background input is enabled the client can accept input when the client does not have focus.</span></span>

<span data-ttu-id="fa2cd-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fa2cd-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2cd-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa2cd-126">Syntax</span></span>


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a><span data-ttu-id="fa2cd-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fa2cd-127">Property value</span></span>

<span data-ttu-id="fa2cd-128">Defina esse parâmetro como 0 para desabilitar o modo de entrada em segundo plano ou um valor diferente de zero para habilitar o modo de entrada em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fa2cd-128">Set this parameter to 0 to disable background input mode or a nonzero value to enable background input mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa2cd-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fa2cd-129">Error codes</span></span>

<span data-ttu-id="fa2cd-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa2cd-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa2cd-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa2cd-131">Remarks</span></span>

<span data-ttu-id="fa2cd-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fa2cd-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2cd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa2cd-133">Requirements</span></span>



| <span data-ttu-id="fa2cd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa2cd-134">Requirement</span></span> | <span data-ttu-id="fa2cd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fa2cd-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2cd-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa2cd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2cd-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa2cd-137">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="fa2cd-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa2cd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2cd-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa2cd-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fa2cd-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fa2cd-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa2cd-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa2cd-141"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="fa2cd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fa2cd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa2cd-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa2cd-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="fa2cd-144">IID</span><span class="sxs-lookup"><span data-stu-id="fa2cd-144">IID</span></span><br/>                      | <span data-ttu-id="fa2cd-145">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="fa2cd-145">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa2cd-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa2cd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2cd-147">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-147">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-149">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fa2cd-155">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fa2cd-155">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





