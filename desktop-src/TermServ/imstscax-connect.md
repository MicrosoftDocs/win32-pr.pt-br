---
title: Método de conexão IMsTscAx
description: Inicia uma conexão usando as propriedades atualmente definidas no controle.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método Connect
- Método Connect Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918194"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="f6e7d-124">Método IMsTscAx:: Connect</span><span class="sxs-lookup"><span data-stu-id="f6e7d-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="f6e7d-125">Inicia uma conexão usando as propriedades atualmente definidas no controle.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e7d-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6e7d-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="f6e7d-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6e7d-127">Parameters</span></span>

<span data-ttu-id="f6e7d-128">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6e7d-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6e7d-129">Return value</span></span>

<span data-ttu-id="f6e7d-130">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6e7d-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6e7d-131">Remarks</span></span>

<span data-ttu-id="f6e7d-132">A única propriedade necessária é o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-132">The only required property is the server name.</span></span> <span data-ttu-id="f6e7d-133">Consulte a propriedade [**Server**](imstscax-server.md) .</span><span class="sxs-lookup"><span data-stu-id="f6e7d-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="f6e7d-134">O controle se conecta de forma assíncrona, de modo que um retorno de uma chamada de conexão indica apenas que a conexão foi iniciada com êxito, não que ela tenha sido concluída.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="f6e7d-135">Você deve responder a eventos na interface [**IMsTscAxEvents**](imstscaxevents-interface.md) para determinar quando o controle foi conectado com êxito (ou se foi desconectado.)</span><span class="sxs-lookup"><span data-stu-id="f6e7d-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="f6e7d-136">Esse método retornará **E \_ falhará** se for chamado enquanto o controle já estiver conectado ou no estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="f6e7d-137">Depois que o **Connect** for chamado, a maioria das propriedades de controle não poderá mais ser definida até que o controle retorne ao estado desconectado.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="f6e7d-138">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f6e7d-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e7d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6e7d-139">Requirements</span></span>



| <span data-ttu-id="f6e7d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6e7d-140">Requirement</span></span> | <span data-ttu-id="f6e7d-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f6e7d-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e7d-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6e7d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e7d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6e7d-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f6e7d-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6e7d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e7d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6e7d-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f6e7d-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f6e7d-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6e7d-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6e7d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f6e7d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e7d-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6e7d-150">IID</span><span class="sxs-lookup"><span data-stu-id="f6e7d-150">IID</span></span><br/>                      | <span data-ttu-id="f6e7d-151">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f6e7d-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f6e7d-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6e7d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e7d-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-162">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="f6e7d-163">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





