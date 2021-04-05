---
title: Propriedade de domínio IMsTscAx
description: Especifica o domínio no qual o usuário atual faz logon.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, propriedade de domínio
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919044"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="bb4be-124">IMsTscAx: Propriedade omain de:D</span><span class="sxs-lookup"><span data-stu-id="bb4be-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="bb4be-125">Especifica o domínio no qual o usuário atual faz logon.</span><span class="sxs-lookup"><span data-stu-id="bb4be-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="bb4be-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bb4be-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb4be-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb4be-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="bb4be-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bb4be-128">Property value</span></span>

<span data-ttu-id="bb4be-129">O novo nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="bb4be-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb4be-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bb4be-130">Error codes</span></span>

<span data-ttu-id="bb4be-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bb4be-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb4be-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb4be-132">Remarks</span></span>

<span data-ttu-id="bb4be-133">A definição da propriedade **Domain** é opcional.</span><span class="sxs-lookup"><span data-stu-id="bb4be-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="bb4be-134">Se não estiver definido, o usuário poderá escolher um domínio quando a caixa de diálogo de logon do Windows aparecer durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="bb4be-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="bb4be-135">O método **obter \_ domínio** aloca a memória necessária para o buffer apontado pelo parâmetro *pDomain* .</span><span class="sxs-lookup"><span data-stu-id="bb4be-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="bb4be-136">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="bb4be-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="bb4be-137">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="bb4be-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="bb4be-138">Essa propriedade só poderá ser definida se o controle não estiver no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="bb4be-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="bb4be-139">Retornará **E \_ falhará** se for chamado quando o controle estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="bb4be-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="bb4be-140">Você pode verificar se o controle está conectado respondendo a eventos de conexão em [**IMsTscAxEvents**](imstscaxevents-interface.md) ou examinando a propriedade [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4be-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="bb4be-141">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bb4be-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb4be-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb4be-142">Requirements</span></span>



| <span data-ttu-id="bb4be-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb4be-143">Requirement</span></span> | <span data-ttu-id="bb4be-144">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4be-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4be-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb4be-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bb4be-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb4be-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bb4be-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb4be-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bb4be-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb4be-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bb4be-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bb4be-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb4be-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb4be-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bb4be-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bb4be-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb4be-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb4be-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bb4be-153">IID</span><span class="sxs-lookup"><span data-stu-id="bb4be-153">IID</span></span><br/>                      | <span data-ttu-id="bb4be-154">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="bb4be-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bb4be-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb4be-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4be-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="bb4be-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="bb4be-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="bb4be-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="bb4be-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="bb4be-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="bb4be-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="bb4be-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="bb4be-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="bb4be-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="bb4be-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="bb4be-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="bb4be-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="bb4be-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="bb4be-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="bb4be-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="bb4be-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="bb4be-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="bb4be-165">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="bb4be-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="bb4be-166">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="bb4be-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="bb4be-167">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="bb4be-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

