---
title: Propriedade IMsRdpClient FullScreen
description: Determina se o controle de cliente está no modo de tela inteira.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade FullScreen
- Serviços de Área de Trabalho Remota da propriedade FullScreen, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086287"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="9d514-124">Propriedade IMsRdpClient:: FullScreen</span><span class="sxs-lookup"><span data-stu-id="9d514-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="9d514-125">Determina se o controle de cliente está no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="9d514-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="9d514-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9d514-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d514-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d514-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="9d514-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9d514-128">Property value</span></span>

<span data-ttu-id="9d514-129">**True** para entrar no modo de tela inteira, **false** para sair do modo de tela inteira e retornar ao modo de janela.</span><span class="sxs-lookup"><span data-stu-id="9d514-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d514-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9d514-130">Error codes</span></span>

<span data-ttu-id="9d514-131">Se os métodos forem bem-sucedidos, será retornado **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="9d514-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="9d514-132">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="9d514-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d514-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d514-133">Remarks</span></span>

<span data-ttu-id="9d514-134">Você pode definir essa propriedade quando o controle estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="9d514-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="9d514-135">Você deve chamar o método [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de chamar o método [**IMsTscSecuredSettings::p UT \_ fullscreen**](imstscsecuredsettings-fullscreen.md) ou o método **IMsRdpClient::p UT \_ fullscreen** .</span><span class="sxs-lookup"><span data-stu-id="9d514-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="9d514-136">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9d514-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d514-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d514-137">Requirements</span></span>



| <span data-ttu-id="9d514-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d514-138">Requirement</span></span> | <span data-ttu-id="9d514-139">Valor</span><span class="sxs-lookup"><span data-stu-id="9d514-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d514-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d514-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9d514-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d514-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9d514-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d514-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9d514-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d514-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9d514-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9d514-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d514-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d514-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d514-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9d514-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d514-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d514-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d514-148">IID</span><span class="sxs-lookup"><span data-stu-id="9d514-148">IID</span></span><br/>                      | <span data-ttu-id="9d514-149">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="9d514-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9d514-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d514-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d514-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="9d514-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="9d514-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="9d514-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="9d514-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="9d514-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="9d514-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9d514-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9d514-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9d514-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9d514-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9d514-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9d514-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9d514-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9d514-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9d514-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9d514-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9d514-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9d514-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9d514-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





