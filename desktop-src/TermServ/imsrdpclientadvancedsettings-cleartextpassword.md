---
title: Propriedade IMsRdpClientAdvancedSettings ClearTextPassword
description: Especifica a senha com a qual se conectar. Para obter mais informações, consulte a interface IMsTscNonScriptable.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ClearTextPassword
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455061"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="e8301-121">Propriedade IMsRdpClientAdvancedSettings:: ClearTextPassword</span><span class="sxs-lookup"><span data-stu-id="e8301-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="e8301-122">Especifica a senha com a qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="e8301-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="e8301-123">Para obter mais informações, consulte a interface [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="e8301-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="e8301-124">Embora o acesso programável a senhas de texto não criptografado esteja disponível por meio dessa propriedade, ainda é responsabilidade do desenvolvedor exercitar a cada cuidado e manter a segurança ao passar senhas em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e8301-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="e8301-125">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="e8301-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8301-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8301-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="e8301-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8301-127">Property value</span></span>

<span data-ttu-id="e8301-128">A nova senha.</span><span class="sxs-lookup"><span data-stu-id="e8301-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8301-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e8301-129">Error codes</span></span>

<span data-ttu-id="e8301-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e8301-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8301-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8301-131">Remarks</span></span>

<span data-ttu-id="e8301-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e8301-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8301-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8301-133">Requirements</span></span>



| <span data-ttu-id="e8301-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8301-134">Requirement</span></span> | <span data-ttu-id="e8301-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e8301-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8301-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8301-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e8301-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8301-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e8301-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8301-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e8301-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8301-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e8301-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e8301-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8301-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8301-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e8301-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e8301-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8301-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8301-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e8301-144">IID</span><span class="sxs-lookup"><span data-stu-id="e8301-144">IID</span></span><br/>                      | <span data-ttu-id="e8301-145">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e8301-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8301-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8301-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8301-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e8301-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e8301-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e8301-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e8301-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e8301-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e8301-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e8301-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e8301-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e8301-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e8301-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e8301-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e8301-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e8301-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e8301-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e8301-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





