---
title: Propriedade IMsTscAx SecuredSettingsEnabled
description: Indica se a interface IMsTscSecuredSettings está disponível. Ou seja, se a página da Web que contém o controle está atualmente em uma das zonas de segurança de URL permitidas do Internet Explorer.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764738"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="269b3-125">Propriedade IMsTscAx:: SecuredSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="269b3-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="269b3-126">Indica se a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponível.</span><span class="sxs-lookup"><span data-stu-id="269b3-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="269b3-127">Ou seja, se a página da Web que contém o controle está atualmente em uma das zonas de segurança de URL permitidas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="269b3-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="269b3-128">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="269b3-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="269b3-129">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="269b3-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="269b3-130">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="269b3-130">Property value</span></span>

<span data-ttu-id="269b3-131">O valor desse parâmetro será **true** se a interface estiver disponível e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="269b3-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="269b3-132">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="269b3-132">Error codes</span></span>

<span data-ttu-id="269b3-133">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="269b3-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="269b3-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="269b3-134">Remarks</span></span>

<span data-ttu-id="269b3-135">Use este método para consultar se a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponível antes de recuperar a propriedade [**SecuredSettings**](imstscax-securedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="269b3-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="269b3-136">Consulte [fornecimento de segurança de cliente RDP](providing-for-rdp-client-security.md) para obter uma lista de zonas de segurança de URL restritas.</span><span class="sxs-lookup"><span data-stu-id="269b3-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="269b3-137">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="269b3-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="269b3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="269b3-138">Requirements</span></span>



| <span data-ttu-id="269b3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="269b3-139">Requirement</span></span> | <span data-ttu-id="269b3-140">Valor</span><span class="sxs-lookup"><span data-stu-id="269b3-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="269b3-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="269b3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="269b3-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="269b3-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="269b3-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="269b3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="269b3-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="269b3-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="269b3-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="269b3-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="269b3-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="269b3-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="269b3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="269b3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="269b3-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="269b3-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="269b3-149">IID</span><span class="sxs-lookup"><span data-stu-id="269b3-149">IID</span></span><br/>                      | <span data-ttu-id="269b3-150">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="269b3-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="269b3-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="269b3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269b3-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="269b3-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="269b3-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="269b3-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="269b3-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="269b3-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="269b3-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="269b3-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="269b3-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="269b3-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="269b3-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="269b3-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="269b3-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="269b3-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="269b3-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="269b3-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="269b3-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="269b3-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="269b3-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="269b3-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="269b3-162">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="269b3-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





