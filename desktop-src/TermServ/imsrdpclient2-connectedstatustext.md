---
title: Propriedade IMsRdpClient2 ConnectedStatusText
description: Contém o texto que é exibido na área do cliente do controle enquanto o controle está no estado conectado.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade ConnectedStatusText
- Propriedade ConnectedStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade ConnectedStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788038"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="57606-122">Propriedade IMsRdpClient2:: ConnectedStatusText</span><span class="sxs-lookup"><span data-stu-id="57606-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="57606-123">Contém o texto que é exibido na área do cliente do controle enquanto o controle está no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="57606-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="57606-124">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="57606-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57606-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="57606-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="57606-126">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="57606-126">Property value</span></span>

<span data-ttu-id="57606-127">A propriedade **ConnectedStatusText** contém o texto que é exibido na área do cliente do controle enquanto o controle está no estado Connected.</span><span class="sxs-lookup"><span data-stu-id="57606-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57606-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="57606-128">Error codes</span></span>

<span data-ttu-id="57606-129">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="57606-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="57606-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="57606-130">Remarks</span></span>

<span data-ttu-id="57606-131">Texto a ser exibido na área do cliente do controle enquanto o controle está no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="57606-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="57606-132">Esse é o texto que é visível, por exemplo, quando o usuário alterna o controle para o modo de tela inteira em um navegador da Web, um cenário que deixa uma parte do controle hospedado no navegador.</span><span class="sxs-lookup"><span data-stu-id="57606-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="57606-133">O método **Get \_ ConnectedStatusText** aloca a memória necessária para o buffer apontado pelo parâmetro *pConnectedStatusText* .</span><span class="sxs-lookup"><span data-stu-id="57606-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="57606-134">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="57606-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="57606-135">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="57606-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="57606-136">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="57606-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="57606-137">Você pode verificar se o controle está conectado chamando o método [**IMsTscAx:: get \_ conectado**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="57606-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="57606-138">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="57606-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57606-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57606-139">Requirements</span></span>



| <span data-ttu-id="57606-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="57606-140">Requirement</span></span> | <span data-ttu-id="57606-141">Valor</span><span class="sxs-lookup"><span data-stu-id="57606-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57606-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57606-142">Minimum supported client</span></span><br/> | <span data-ttu-id="57606-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57606-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="57606-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57606-144">Minimum supported server</span></span><br/> | <span data-ttu-id="57606-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57606-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="57606-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="57606-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="57606-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57606-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="57606-148">DLL</span><span class="sxs-lookup"><span data-stu-id="57606-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57606-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57606-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="57606-150">IID</span><span class="sxs-lookup"><span data-stu-id="57606-150">IID</span></span><br/>                      | <span data-ttu-id="57606-151">IID \_ IMsRdpClient2 é definido como e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="57606-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="57606-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="57606-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57606-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="57606-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="57606-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="57606-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="57606-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="57606-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="57606-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="57606-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="57606-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="57606-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="57606-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="57606-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="57606-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="57606-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="57606-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="57606-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="57606-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="57606-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

