---
title: Propriedade IMsTscAx SecuredSettings
description: Recupera um ponteiro de interface IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade SecuredSettings
- Propriedade SecuredSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085557"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="f8dc3-124">Propriedade IMsTscAx:: SecuredSettings</span><span class="sxs-lookup"><span data-stu-id="f8dc3-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="f8dc3-125">Recupera um ponteiro de interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="f8dc3-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="f8dc3-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8dc3-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8dc3-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="f8dc3-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f8dc3-128">Property value</span></span>

<span data-ttu-id="f8dc3-129">Um ponteiro de interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="f8dc3-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8dc3-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f8dc3-130">Error codes</span></span>

<span data-ttu-id="f8dc3-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8dc3-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8dc3-132">Remarks</span></span>

<span data-ttu-id="f8dc3-133">Se o controle estiver hospedado em uma página da Web e a zona de segurança da URL atual do Internet Explorer não permitir a recuperação do endereço da interface, esse método retornará **E \_ falhará**.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="f8dc3-134">Consulte [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para obter restrições sobre a disponibilidade da interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="f8dc3-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="f8dc3-135">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f8dc3-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8dc3-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8dc3-136">Requirements</span></span>



| <span data-ttu-id="f8dc3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8dc3-137">Requirement</span></span> | <span data-ttu-id="f8dc3-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f8dc3-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8dc3-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8dc3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f8dc3-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8dc3-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f8dc3-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8dc3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f8dc3-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8dc3-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f8dc3-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f8dc3-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8dc3-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8dc3-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f8dc3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f8dc3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8dc3-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8dc3-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f8dc3-147">IID</span><span class="sxs-lookup"><span data-stu-id="f8dc3-147">IID</span></span><br/>                      | <span data-ttu-id="f8dc3-148">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f8dc3-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f8dc3-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8dc3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8dc3-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="f8dc3-160">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="f8dc3-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





