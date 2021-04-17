---
title: Propriedade IMsTscAx StartConnected
description: Indica se o controle irá estabelecer a conexão do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) imediatamente após a inicialização.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade StartConnected
- Propriedade StartConnected Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768547"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="0908f-124">Propriedade IMsTscAx:: StartConnected</span><span class="sxs-lookup"><span data-stu-id="0908f-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="0908f-125">Indica se o controle irá estabelecer a conexão do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) imediatamente após a inicialização.</span><span class="sxs-lookup"><span data-stu-id="0908f-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="0908f-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0908f-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0908f-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="0908f-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="0908f-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0908f-128">Property value</span></span>

<span data-ttu-id="0908f-129">Defina esse parâmetro como **true** se o controle deve se conectar imediatamente na inicialização ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0908f-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0908f-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0908f-130">Error codes</span></span>

<span data-ttu-id="0908f-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0908f-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0908f-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="0908f-132">Remarks</span></span>

<span data-ttu-id="0908f-133">Essa propriedade é mais útil quando as propriedades de controle são definidas na lista de parâmetros de uma <OBJECT> marca, em vez de chamadas de script.</span><span class="sxs-lookup"><span data-stu-id="0908f-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="0908f-134">Essa propriedade só poderá ser usada se o nome do servidor também for especificado usando a Propriedade Server.</span><span class="sxs-lookup"><span data-stu-id="0908f-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="0908f-135">Esse parâmetro deve ser definido antes que o controle seja iniciado, por exemplo, incluindo-o na lista de parâmetros de uma <OBJECT> marca ao usar o controle de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="0908f-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="0908f-136">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0908f-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0908f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0908f-137">Requirements</span></span>



| <span data-ttu-id="0908f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0908f-138">Requirement</span></span> | <span data-ttu-id="0908f-139">Valor</span><span class="sxs-lookup"><span data-stu-id="0908f-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0908f-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0908f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0908f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0908f-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0908f-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0908f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0908f-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0908f-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0908f-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0908f-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="0908f-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0908f-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0908f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0908f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0908f-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0908f-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0908f-148">IID</span><span class="sxs-lookup"><span data-stu-id="0908f-148">IID</span></span><br/>                      | <span data-ttu-id="0908f-149">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0908f-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0908f-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="0908f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0908f-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0908f-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0908f-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0908f-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0908f-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0908f-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0908f-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0908f-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0908f-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0908f-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0908f-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0908f-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0908f-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0908f-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0908f-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0908f-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0908f-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0908f-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0908f-160">Inserindo o controle ActiveX Área de Trabalho Remota em uma página da Web</span><span class="sxs-lookup"><span data-stu-id="0908f-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="0908f-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0908f-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





