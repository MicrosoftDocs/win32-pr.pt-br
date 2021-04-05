---
title: Propriedade IMsTscAx FullScreenTitle
description: Especifica o título da janela exibido quando o controle está no modo de tela inteira.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade FullScreenTitle
- Propriedade FullScreenTitle Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade FullScreenTitle
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085771"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="805f2-124">Propriedade IMsTscAx:: FullScreenTitle</span><span class="sxs-lookup"><span data-stu-id="805f2-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="805f2-125">Especifica o título da janela exibido quando o controle está no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="805f2-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="805f2-126">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="805f2-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="805f2-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="805f2-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="805f2-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="805f2-128">Property value</span></span>

<span data-ttu-id="805f2-129">O título da janela.</span><span class="sxs-lookup"><span data-stu-id="805f2-129">The window title.</span></span> <span data-ttu-id="805f2-130">O comprimento máximo dessa cadeia de caracteres é o \_ caminho máximo-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="805f2-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="805f2-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="805f2-131">Error codes</span></span>

<span data-ttu-id="805f2-132">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="805f2-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="805f2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="805f2-133">Remarks</span></span>

<span data-ttu-id="805f2-134">Essa propriedade é usada para definir o título da janela do controle quando a conexão é aberta no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="805f2-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="805f2-135">Não use essa propriedade para o modo de tela inteira manipulado por contêiner.</span><span class="sxs-lookup"><span data-stu-id="805f2-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="805f2-136">Quando o método [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) é chamado, a janela contêiner exibe o título da janela.</span><span class="sxs-lookup"><span data-stu-id="805f2-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="805f2-137">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="805f2-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="805f2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805f2-138">Requirements</span></span>



| <span data-ttu-id="805f2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="805f2-139">Requirement</span></span> | <span data-ttu-id="805f2-140">Valor</span><span class="sxs-lookup"><span data-stu-id="805f2-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="805f2-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="805f2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="805f2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="805f2-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="805f2-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="805f2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="805f2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="805f2-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="805f2-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="805f2-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="805f2-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805f2-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="805f2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="805f2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="805f2-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805f2-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="805f2-149">IID</span><span class="sxs-lookup"><span data-stu-id="805f2-149">IID</span></span><br/>                      | <span data-ttu-id="805f2-150">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="805f2-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="805f2-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="805f2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805f2-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="805f2-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="805f2-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="805f2-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="805f2-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="805f2-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="805f2-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="805f2-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="805f2-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="805f2-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="805f2-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="805f2-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="805f2-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="805f2-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="805f2-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="805f2-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="805f2-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="805f2-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="805f2-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="805f2-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





