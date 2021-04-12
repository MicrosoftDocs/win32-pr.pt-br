---
title: Propriedade IMsRdpClient SecuredSettings2
description: Recupera um ponteiro para a interface IMsRdpClientSecuredSettings. Essa interface pode ser usada para definir configurações protegidas para o controle de cliente.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade SecuredSettings2
- Propriedade SecuredSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499237"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="30cdd-125">Propriedade IMsRdpClient:: SecuredSettings2</span><span class="sxs-lookup"><span data-stu-id="30cdd-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="30cdd-126">Recupera um ponteiro para a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="30cdd-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="30cdd-127">Essa interface pode ser usada para definir configurações protegidas para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="30cdd-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="30cdd-128">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="30cdd-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cdd-129">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30cdd-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="30cdd-130">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="30cdd-130">Property value</span></span>

<span data-ttu-id="30cdd-131">Um ponteiro de interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="30cdd-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30cdd-132">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="30cdd-132">Error codes</span></span>

<span data-ttu-id="30cdd-133">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="30cdd-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="30cdd-134">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="30cdd-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="30cdd-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="30cdd-135">Remarks</span></span>

<span data-ttu-id="30cdd-136">Para obter mais informações, consulte a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) e [fornecendo o RDP Client Security](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="30cdd-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="30cdd-137">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30cdd-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30cdd-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30cdd-138">Requirements</span></span>



| <span data-ttu-id="30cdd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="30cdd-139">Requirement</span></span> | <span data-ttu-id="30cdd-140">Valor</span><span class="sxs-lookup"><span data-stu-id="30cdd-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30cdd-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30cdd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="30cdd-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30cdd-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="30cdd-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30cdd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="30cdd-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30cdd-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="30cdd-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="30cdd-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="30cdd-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30cdd-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30cdd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="30cdd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30cdd-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30cdd-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30cdd-149">IID</span><span class="sxs-lookup"><span data-stu-id="30cdd-149">IID</span></span><br/>                      | <span data-ttu-id="30cdd-150">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="30cdd-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="30cdd-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="30cdd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cdd-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="30cdd-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="30cdd-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="30cdd-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="30cdd-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="30cdd-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="30cdd-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="30cdd-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="30cdd-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="30cdd-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="30cdd-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="30cdd-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="30cdd-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="30cdd-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="30cdd-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="30cdd-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="30cdd-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="30cdd-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="30cdd-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="30cdd-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





