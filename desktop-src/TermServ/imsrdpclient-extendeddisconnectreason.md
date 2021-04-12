---
title: Propriedade IMsRdpClient ExtendedDisconnectReason
description: Contém informações estendidas sobre o motivo do controle para desconexão.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade ExtendedDisconnectReason
- Propriedade ExtendedDisconnectReason Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade ExtendedDisconnectReason
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499728"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="9c42a-124">Propriedade IMsRdpClient:: ExtendedDisconnectReason</span><span class="sxs-lookup"><span data-stu-id="9c42a-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="9c42a-125">Contém informações estendidas sobre o motivo do controle para desconexão.</span><span class="sxs-lookup"><span data-stu-id="9c42a-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="9c42a-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9c42a-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c42a-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c42a-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="9c42a-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9c42a-128">Property value</span></span>

<span data-ttu-id="9c42a-129">Aponta para o valor [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) que indica o motivo da desconexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="9c42a-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c42a-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9c42a-130">Error codes</span></span>

<span data-ttu-id="9c42a-131">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="9c42a-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="9c42a-132">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="9c42a-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c42a-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c42a-133">Remarks</span></span>

<span data-ttu-id="9c42a-134">Normalmente, esse método é chamado no manipulador de eventos [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) para recuperar informações adicionais sobre o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="9c42a-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="9c42a-135">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9c42a-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c42a-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c42a-136">Requirements</span></span>



| <span data-ttu-id="9c42a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c42a-137">Requirement</span></span> | <span data-ttu-id="9c42a-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9c42a-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c42a-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c42a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9c42a-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c42a-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9c42a-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c42a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9c42a-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c42a-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9c42a-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9c42a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c42a-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c42a-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c42a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9c42a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c42a-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c42a-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c42a-147">IID</span><span class="sxs-lookup"><span data-stu-id="9c42a-147">IID</span></span><br/>                      | <span data-ttu-id="9c42a-148">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="9c42a-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9c42a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c42a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c42a-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="9c42a-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="9c42a-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="9c42a-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="9c42a-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="9c42a-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="9c42a-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9c42a-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9c42a-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9c42a-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9c42a-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9c42a-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9c42a-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9c42a-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9c42a-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9c42a-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9c42a-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9c42a-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9c42a-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9c42a-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="9c42a-160">**IMsTscAxEvents:: ondisconnectd**</span><span class="sxs-lookup"><span data-stu-id="9c42a-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





