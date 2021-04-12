---
title: Propriedade de versão IMsTscAx
description: Especifica o número de versão do controle atual.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de versão
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade Version
- Serviços de Área de Trabalho Remota da Propriedade Version, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade Version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455153"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="0cb3b-124">Propriedade IMsTscAx:: Version</span><span class="sxs-lookup"><span data-stu-id="0cb3b-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="0cb3b-125">Especifica o número de versão do controle atual.</span><span class="sxs-lookup"><span data-stu-id="0cb3b-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="0cb3b-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0cb3b-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb3b-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cb3b-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="0cb3b-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0cb3b-128">Property value</span></span>

<span data-ttu-id="0cb3b-129">O número de versão.</span><span class="sxs-lookup"><span data-stu-id="0cb3b-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0cb3b-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0cb3b-130">Error codes</span></span>

<span data-ttu-id="0cb3b-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0cb3b-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb3b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb3b-132">Remarks</span></span>

<span data-ttu-id="0cb3b-133">Esse método aloca a memória necessária para o buffer apontado pelo parâmetro *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="0cb3b-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="0cb3b-134">Chamar aplicativos C/C++ deve liberar a memória com uma chamada para a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="0cb3b-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="0cb3b-135">Isso não é necessário para clientes de Visual Basic e de script.</span><span class="sxs-lookup"><span data-stu-id="0cb3b-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="0cb3b-136">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0cb3b-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb3b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb3b-137">Requirements</span></span>



| <span data-ttu-id="0cb3b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb3b-138">Requirement</span></span> | <span data-ttu-id="0cb3b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb3b-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb3b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb3b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb3b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cb3b-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0cb3b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb3b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb3b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cb3b-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0cb3b-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0cb3b-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="0cb3b-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb3b-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0cb3b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb3b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb3b-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb3b-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0cb3b-148">IID</span><span class="sxs-lookup"><span data-stu-id="0cb3b-148">IID</span></span><br/>                      | <span data-ttu-id="0cb3b-149">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0cb3b-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0cb3b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb3b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb3b-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0cb3b-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0cb3b-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

