---
title: Propriedade de nome de usuário IMsTscAx
description: Especifica a credencial de logon do nome de usuário.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Propriedade de nome de usuário Serviços de Área de Trabalho Remota
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade UserName
- Propriedade UserName Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455917"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="aee03-124">Propriedade IMsTscAx:: UserName</span><span class="sxs-lookup"><span data-stu-id="aee03-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="aee03-125">Especifica a credencial de logon do nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="aee03-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="aee03-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aee03-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee03-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="aee03-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="aee03-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aee03-128">Property value</span></span>

<span data-ttu-id="aee03-129">O novo nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="aee03-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aee03-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="aee03-130">Error codes</span></span>

<span data-ttu-id="aee03-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aee03-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="aee03-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="aee03-132">Remarks</span></span>

<span data-ttu-id="aee03-133">A definição da propriedade **username** é opcional.</span><span class="sxs-lookup"><span data-stu-id="aee03-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="aee03-134">Se não for especificado, o usuário poderá fornecer um nome de usuário quando a caixa de diálogo de logon do Windows for exibida durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="aee03-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="aee03-135">Essa propriedade só poderá ser definida se o controle não estiver no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="aee03-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="aee03-136">Retornará **E \_ falhará** se for chamado quando o controle estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="aee03-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="aee03-137">Você pode verificar se o controle está conectado respondendo a eventos de conexão em [**IMsTscAxEvents**](imstscaxevents-interface.md) ou examinando a propriedade [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="aee03-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="aee03-138">O método **Get \_ username** Property aloca a memória necessária para o buffer apontado pelo parâmetro *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="aee03-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="aee03-139">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="aee03-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="aee03-140">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="aee03-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="aee03-141">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="aee03-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aee03-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee03-142">Requirements</span></span>



| <span data-ttu-id="aee03-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee03-143">Requirement</span></span> | <span data-ttu-id="aee03-144">Valor</span><span class="sxs-lookup"><span data-stu-id="aee03-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee03-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee03-145">Minimum supported client</span></span><br/> | <span data-ttu-id="aee03-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee03-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aee03-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee03-147">Minimum supported server</span></span><br/> | <span data-ttu-id="aee03-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee03-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aee03-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aee03-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="aee03-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee03-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aee03-151">DLL</span><span class="sxs-lookup"><span data-stu-id="aee03-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee03-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee03-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aee03-153">IID</span><span class="sxs-lookup"><span data-stu-id="aee03-153">IID</span></span><br/>                      | <span data-ttu-id="aee03-154">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="aee03-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="aee03-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="aee03-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee03-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="aee03-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="aee03-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="aee03-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="aee03-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="aee03-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="aee03-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="aee03-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="aee03-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="aee03-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="aee03-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="aee03-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="aee03-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="aee03-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="aee03-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="aee03-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="aee03-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="aee03-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="aee03-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="aee03-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

