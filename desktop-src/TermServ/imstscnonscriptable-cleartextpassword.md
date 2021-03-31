---
title: Propriedade IMsTscNonScriptable ClearTextPassword
description: Define a Área de Trabalho Remota senha do controle ActiveX em formato de texto sem formatação.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645156"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="8f9d1-124">Propriedade IMsTscNonScriptable:: ClearTextPassword</span><span class="sxs-lookup"><span data-stu-id="8f9d1-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="8f9d1-125">Define a Área de Trabalho Remota senha do controle ActiveX em formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="8f9d1-126">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9d1-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f9d1-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="8f9d1-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8f9d1-128">Property value</span></span>

<span data-ttu-id="8f9d1-129">A senha a ser usada para conexão, especificada em formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8f9d1-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8f9d1-130">Error codes</span></span>

<span data-ttu-id="8f9d1-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9d1-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f9d1-132">Remarks</span></span>

<span data-ttu-id="8f9d1-133">A senha é passada para o servidor no canal de comunicações RDP criptografado com segurança.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="8f9d1-134">Depois que uma senha de texto sem formatação é definida, ela não pode ser recuperada no formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="8f9d1-135">A propriedade **clearTextPassword** só pode ser definida quando o controle ActiveX área de trabalho remota não está no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="8f9d1-136">A definição dessa propriedade falhará se o controle estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="8f9d1-137">Para verificar o estado conectado, recupere a propriedade [**IMsTscAx:: Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9d1-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="8f9d1-138">Você também pode chamar esse método para definir uma senha de texto sem formatação antes de convertê-la para uma senha codificada em portátil ou para uma senha codificada binária (não-Portable).</span><span class="sxs-lookup"><span data-stu-id="8f9d1-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="8f9d1-139">No entanto, observe que as senhas codificadas não devem ser consideradas criptografadas com segurança.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="8f9d1-140">Se você chamar primeiro este método para definir uma senha em formato de texto sem formatação, poderá converter a senha no formato codificado.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="8f9d1-141">**Para converter uma senha de texto sem formatação em formato codificado**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="8f9d1-142">Defina a senha em formato de texto sem formatação na propriedade **clearTextPassword** .</span><span class="sxs-lookup"><span data-stu-id="8f9d1-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="8f9d1-143">Para recuperar a senha em formato binário (não Portable) codificado, recupere a propriedade [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e as propriedades [**BinarySalt**](imstscnonscriptable-binarysalt.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9d1-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="8f9d1-144">A parte da senha codificada e a parte Salt são necessárias para definir uma senha no formato binário codificado.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="8f9d1-145">Para recuperar a senha no formato de codificação portátil, recupere o método [**PortablePassword**](imstscnonscriptable-portablepassword.md) e as propriedades [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9d1-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="8f9d1-146">Ambas as partes são necessárias para definir uma senha no formato codificado portátil.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="8f9d1-147">Depois de seguir as três etapas anteriores, você pode definir a senha no formato codificado definindo as propriedades [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt**](imstscnonscriptable-binarysalt.md) ou as propriedades [**PortablePassword**](imstscnonscriptable-portablepassword.md) e [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9d1-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="8f9d1-148">Ambas as partes são necessárias.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-148">Both parts are required.</span></span>

<span data-ttu-id="8f9d1-149">Para habilitar o logon automático, você também deve definir as propriedades de [**nome de usuário**](imstscax-username.md) e [**domínio**](imstscax-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9d1-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="8f9d1-150">Se a senha não autenticar o usuário, a caixa de diálogo logon do Windows será exibida no servidor para solicitar a senha ao usuário.</span><span class="sxs-lookup"><span data-stu-id="8f9d1-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="8f9d1-151">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8f9d1-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9d1-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f9d1-152">Requirements</span></span>



| <span data-ttu-id="8f9d1-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9d1-153">Requirement</span></span> | <span data-ttu-id="8f9d1-154">Valor</span><span class="sxs-lookup"><span data-stu-id="8f9d1-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9d1-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f9d1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9d1-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f9d1-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8f9d1-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f9d1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9d1-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f9d1-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8f9d1-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8f9d1-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f9d1-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9d1-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8f9d1-161">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9d1-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9d1-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9d1-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8f9d1-163">IID</span><span class="sxs-lookup"><span data-stu-id="8f9d1-163">IID</span></span><br/>                      | <span data-ttu-id="8f9d1-164">IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="8f9d1-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f9d1-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f9d1-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9d1-166">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="8f9d1-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="8f9d1-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="8f9d1-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="8f9d1-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="8f9d1-171">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="8f9d1-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





