---
title: Propriedade conectada IMsTscAx (Tsvirtualchannels. h)
description: Recupera o estado de conexão do controle atual.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade conectada
- Propriedade conectada Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade conectada
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761934"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="5e880-124">Propriedade IMsTscAx:: Connected</span><span class="sxs-lookup"><span data-stu-id="5e880-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="5e880-125">Recupera o estado de conexão do controle atual.</span><span class="sxs-lookup"><span data-stu-id="5e880-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="5e880-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5e880-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e880-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e880-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="5e880-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5e880-128">Property value</span></span>

<span data-ttu-id="5e880-129">Indica o estado de conexão do controle.</span><span class="sxs-lookup"><span data-stu-id="5e880-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="5e880-130">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e880-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="5e880-131">0</span><span class="sxs-lookup"><span data-stu-id="5e880-131">0</span></span>
</dt> <dd>

<span data-ttu-id="5e880-132">O controle não está conectado.</span><span class="sxs-lookup"><span data-stu-id="5e880-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="5e880-133">1</span><span class="sxs-lookup"><span data-stu-id="5e880-133">1</span></span>
</dt> <dd>

<span data-ttu-id="5e880-134">O controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="5e880-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="5e880-135">2</span><span class="sxs-lookup"><span data-stu-id="5e880-135">2</span></span>
</dt> <dd>

<span data-ttu-id="5e880-136">O controle está estabelecendo uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5e880-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="5e880-137">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5e880-137">Error codes</span></span>

<span data-ttu-id="5e880-138">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5e880-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e880-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e880-139">Remarks</span></span>

<span data-ttu-id="5e880-140">A maneira preferida de determinar o estado de conexão do controle é responder aos eventos de conexão em [**IMsTscAxEvents**](imstscaxevents-interface.md).</span><span class="sxs-lookup"><span data-stu-id="5e880-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="5e880-141">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5e880-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e880-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e880-142">Requirements</span></span>



| <span data-ttu-id="5e880-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e880-143">Requirement</span></span> | <span data-ttu-id="5e880-144">Valor</span><span class="sxs-lookup"><span data-stu-id="5e880-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e880-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e880-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5e880-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e880-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="5e880-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e880-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5e880-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e880-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="5e880-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e880-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e880-150"><dt>Tsvirtualchannels. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e880-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="5e880-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5e880-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e880-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e880-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5e880-153">DLL</span><span class="sxs-lookup"><span data-stu-id="5e880-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e880-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e880-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5e880-155">IID</span><span class="sxs-lookup"><span data-stu-id="5e880-155">IID</span></span><br/>                      | <span data-ttu-id="5e880-156">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="5e880-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="5e880-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e880-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e880-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="5e880-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="5e880-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="5e880-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="5e880-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="5e880-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="5e880-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="5e880-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="5e880-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5e880-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5e880-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5e880-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5e880-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5e880-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5e880-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5e880-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5e880-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5e880-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5e880-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="5e880-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





