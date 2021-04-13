---
title: Propriedade IMsTscAx ConnectingText
description: Especifica o texto que aparece centralizado no controle enquanto o controle está se conectando.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade ConnectingText
- Propriedade ConnectingText Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade ConnectingText
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369777"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="fa30b-124">Propriedade IMsTscAx:: ConnectingText</span><span class="sxs-lookup"><span data-stu-id="fa30b-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="fa30b-125">Especifica o texto que aparece centralizado no controle enquanto o controle está se conectando.</span><span class="sxs-lookup"><span data-stu-id="fa30b-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="fa30b-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fa30b-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa30b-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa30b-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="fa30b-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fa30b-128">Property value</span></span>

<span data-ttu-id="fa30b-129">O novo texto de exibição.</span><span class="sxs-lookup"><span data-stu-id="fa30b-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa30b-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fa30b-130">Error codes</span></span>

<span data-ttu-id="fa30b-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa30b-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="fa30b-132">Retornar um **HRESULT** diferente de zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="fa30b-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa30b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa30b-133">Remarks</span></span>

<span data-ttu-id="fa30b-134">Um exemplo de texto de conexão é "conectando-se ao servidor...".</span><span class="sxs-lookup"><span data-stu-id="fa30b-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="fa30b-135">A definição da propriedade **ConnectingText** é opcional.</span><span class="sxs-lookup"><span data-stu-id="fa30b-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="fa30b-136">Se não estiver definido, o controle aparecerá em branco antes de uma conexão ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="fa30b-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="fa30b-137">Essa propriedade só poderá ser definida se o controle não estiver no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="fa30b-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="fa30b-138">Retornará **E \_ falhará** se for chamado quando o controle estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="fa30b-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="fa30b-139">Você pode verificar se o controle está conectado respondendo a eventos de conexão em [**IMsTscAxEvents**](imstscaxevents-interface.md) ou examinando a propriedade [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="fa30b-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="fa30b-140">O método de propriedade **Get \_ ConnectingText** aloca a memória necessária para o buffer apontado pelo parâmetro *pConnectingText* .</span><span class="sxs-lookup"><span data-stu-id="fa30b-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="fa30b-141">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="fa30b-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="fa30b-142">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="fa30b-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="fa30b-143">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fa30b-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa30b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa30b-144">Requirements</span></span>



| <span data-ttu-id="fa30b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa30b-145">Requirement</span></span> | <span data-ttu-id="fa30b-146">Valor</span><span class="sxs-lookup"><span data-stu-id="fa30b-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa30b-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa30b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fa30b-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa30b-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fa30b-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa30b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fa30b-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa30b-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fa30b-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fa30b-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa30b-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa30b-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa30b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fa30b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa30b-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa30b-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa30b-155">IID</span><span class="sxs-lookup"><span data-stu-id="fa30b-155">IID</span></span><br/>                      | <span data-ttu-id="fa30b-156">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="fa30b-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fa30b-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa30b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa30b-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="fa30b-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="fa30b-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="fa30b-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="fa30b-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="fa30b-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="fa30b-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="fa30b-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="fa30b-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="fa30b-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="fa30b-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="fa30b-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="fa30b-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="fa30b-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="fa30b-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="fa30b-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="fa30b-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="fa30b-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="fa30b-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="fa30b-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

