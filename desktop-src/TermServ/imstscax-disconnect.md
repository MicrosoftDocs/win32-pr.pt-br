---
title: Método de desconexão de IMsTscAx
description: Desconecta a conexão ativa.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de desconexão
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método Disconnect
- Método Disconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método Disconnect
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499508"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="bc8a7-124">Método IMsTscAx::D isconnect</span><span class="sxs-lookup"><span data-stu-id="bc8a7-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="bc8a7-125">Desconecta a conexão ativa.</span><span class="sxs-lookup"><span data-stu-id="bc8a7-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8a7-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc8a7-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="bc8a7-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc8a7-127">Parameters</span></span>

<span data-ttu-id="bc8a7-128">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bc8a7-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc8a7-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc8a7-129">Return value</span></span>

<span data-ttu-id="bc8a7-130">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bc8a7-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8a7-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc8a7-131">Remarks</span></span>

<span data-ttu-id="bc8a7-132">Esse método retornará um valor de erro de falha se for chamado quando o controle não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="bc8a7-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="bc8a7-133">Também é possível desconectar o controle fechando sua janela principal.</span><span class="sxs-lookup"><span data-stu-id="bc8a7-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="bc8a7-134">Por exemplo, se o controle estiver hospedado em uma página da Web, não será necessário chamar esse método antes de sair da página; o fechamento do controle dispara uma desconexão.</span><span class="sxs-lookup"><span data-stu-id="bc8a7-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="bc8a7-135">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bc8a7-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8a7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8a7-136">Requirements</span></span>



| <span data-ttu-id="bc8a7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8a7-137">Requirement</span></span> | <span data-ttu-id="bc8a7-138">Valor</span><span class="sxs-lookup"><span data-stu-id="bc8a7-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8a7-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc8a7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8a7-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc8a7-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bc8a7-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc8a7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8a7-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc8a7-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bc8a7-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bc8a7-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc8a7-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8a7-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc8a7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8a7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8a7-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8a7-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc8a7-147">IID</span><span class="sxs-lookup"><span data-stu-id="bc8a7-147">IID</span></span><br/>                      | <span data-ttu-id="bc8a7-148">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="bc8a7-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bc8a7-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc8a7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8a7-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-159">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="bc8a7-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="bc8a7-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





