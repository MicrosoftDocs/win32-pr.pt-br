---
title: Propriedade IMsRdpClient AdvancedSettings2
description: Recupera um ponteiro para a interface IMsRdpClientAdvancedSettings. A interface pode ser usada para definir configurações avançadas para o controle de cliente.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings2
- Propriedade AdvancedSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800006"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="b4e92-125">Propriedade IMsRdpClient:: AdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="b4e92-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="b4e92-126">Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e92-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="b4e92-127">A interface pode ser usada para definir configurações avançadas para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="b4e92-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="b4e92-128">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b4e92-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e92-129">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4e92-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="b4e92-130">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b4e92-130">Property value</span></span>

<span data-ttu-id="b4e92-131">Ponteiro para a interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e92-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="b4e92-132">A interface pode ser usada para definir configurações avançadas para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="b4e92-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4e92-133">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b4e92-133">Error codes</span></span>

<span data-ttu-id="b4e92-134">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="b4e92-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="b4e92-135">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="b4e92-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e92-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4e92-136">Remarks</span></span>

<span data-ttu-id="b4e92-137">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b4e92-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e92-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4e92-138">Requirements</span></span>



| <span data-ttu-id="b4e92-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4e92-139">Requirement</span></span> | <span data-ttu-id="b4e92-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b4e92-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e92-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4e92-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e92-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4e92-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b4e92-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4e92-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e92-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4e92-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b4e92-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b4e92-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4e92-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4e92-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4e92-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b4e92-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4e92-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4e92-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4e92-149">IID</span><span class="sxs-lookup"><span data-stu-id="b4e92-149">IID</span></span><br/>                      | <span data-ttu-id="b4e92-150">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="b4e92-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="b4e92-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4e92-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e92-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="b4e92-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="b4e92-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="b4e92-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="b4e92-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="b4e92-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="b4e92-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="b4e92-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="b4e92-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b4e92-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b4e92-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b4e92-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b4e92-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b4e92-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b4e92-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b4e92-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b4e92-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b4e92-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b4e92-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b4e92-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





