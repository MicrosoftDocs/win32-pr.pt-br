---
title: Propriedade IMsTscAx DisconnectedText
description: Especifica o texto que aparece centralizado no controle antes que uma conexão seja encerrada.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade DisconnectedText
- Propriedade DisconnectedText Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade DisconnectedText
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644806"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="273ad-124">IMsTscAx: Propriedade isconnectedText de:D</span><span class="sxs-lookup"><span data-stu-id="273ad-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="273ad-125">Especifica o texto que aparece centralizado no controle antes que uma conexão seja encerrada.</span><span class="sxs-lookup"><span data-stu-id="273ad-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="273ad-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="273ad-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="273ad-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="273ad-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="273ad-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="273ad-128">Property value</span></span>

<span data-ttu-id="273ad-129">O novo texto de exibição.</span><span class="sxs-lookup"><span data-stu-id="273ad-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="273ad-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="273ad-130">Error codes</span></span>

<span data-ttu-id="273ad-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="273ad-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="273ad-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="273ad-132">Remarks</span></span>

<span data-ttu-id="273ad-133">A definição da propriedade **DisconnectedText** é opcional.</span><span class="sxs-lookup"><span data-stu-id="273ad-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="273ad-134">Se não for especificado, o controle aparecerá em branco antes que uma conexão seja estabelecida.</span><span class="sxs-lookup"><span data-stu-id="273ad-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="273ad-135">Essa propriedade só poderá ser definida se o controle não estiver no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="273ad-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="273ad-136">O método retornará **E \_ falhará** se for chamado depois que o controle for conectado.</span><span class="sxs-lookup"><span data-stu-id="273ad-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="273ad-137">Você pode verificar se o controle está conectado respondendo a eventos de conexão em [**IMsTscAxEvents**](imstscaxevents-interface.md) ou examinando a propriedade [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="273ad-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="273ad-138">Esse método aloca a memória necessária para o buffer apontado pelo parâmetro *pDisconnectedText* .</span><span class="sxs-lookup"><span data-stu-id="273ad-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="273ad-139">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="273ad-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="273ad-140">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="273ad-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="273ad-141">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="273ad-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="273ad-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="273ad-142">Requirements</span></span>



| <span data-ttu-id="273ad-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="273ad-143">Requirement</span></span> | <span data-ttu-id="273ad-144">Valor</span><span class="sxs-lookup"><span data-stu-id="273ad-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="273ad-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="273ad-145">Minimum supported client</span></span><br/> | <span data-ttu-id="273ad-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="273ad-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="273ad-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="273ad-147">Minimum supported server</span></span><br/> | <span data-ttu-id="273ad-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="273ad-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="273ad-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="273ad-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="273ad-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="273ad-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="273ad-151">DLL</span><span class="sxs-lookup"><span data-stu-id="273ad-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="273ad-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="273ad-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="273ad-153">IID</span><span class="sxs-lookup"><span data-stu-id="273ad-153">IID</span></span><br/>                      | <span data-ttu-id="273ad-154">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="273ad-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="273ad-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="273ad-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273ad-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="273ad-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="273ad-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="273ad-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="273ad-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="273ad-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="273ad-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="273ad-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="273ad-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="273ad-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="273ad-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="273ad-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="273ad-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="273ad-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="273ad-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="273ad-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="273ad-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="273ad-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="273ad-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="273ad-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

