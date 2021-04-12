---
title: Propriedade IMsTscAx DesktopWidth
description: Especifica a largura do controle atual, em pixels, na área de trabalho remota inicial.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade DesktopWidth
- Propriedade DesktopWidth Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499364"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="378a7-124">IMsTscAx: Propriedade esktopWidth de:D</span><span class="sxs-lookup"><span data-stu-id="378a7-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="378a7-125">Especifica a largura do controle atual, em pixels, na área de trabalho remota inicial.</span><span class="sxs-lookup"><span data-stu-id="378a7-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="378a7-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="378a7-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="378a7-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="378a7-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="378a7-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="378a7-128">Property value</span></span>

<span data-ttu-id="378a7-129">A nova largura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="378a7-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="378a7-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="378a7-130">Error codes</span></span>

<span data-ttu-id="378a7-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="378a7-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="378a7-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="378a7-132">Remarks</span></span>

<span data-ttu-id="378a7-133">A definição da propriedade **DesktopWidth** é opcional, mas deve ser definida antes de chamar o método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="378a7-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="378a7-134">Se uma largura de área de trabalho não for especificada ou for definida como zero, a largura da área de trabalho será definida com a largura do controle.</span><span class="sxs-lookup"><span data-stu-id="378a7-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="378a7-135">Os valores mínimo e máximo dependem da versão do sistema operacional do cliente de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="378a7-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="378a7-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="378a7-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="378a7-137">mínimo de 200, 8192 máximo</span><span class="sxs-lookup"><span data-stu-id="378a7-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="378a7-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="378a7-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="378a7-139">mínimo de 200, 2048 máximo</span><span class="sxs-lookup"><span data-stu-id="378a7-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="378a7-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="378a7-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="378a7-141">mínimo de 200, 1200 máximo</span><span class="sxs-lookup"><span data-stu-id="378a7-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="378a7-142">Depois que uma conexão é estabelecida, as alterações na largura do controle não alteram a largura da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="378a7-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="378a7-143">Em vez disso, o controle abre as barras de rolagem ou centraliza a área de trabalho remota, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="378a7-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="378a7-144">Para alterar o tamanho da área de trabalho de uma conexão ativa, use o método [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="378a7-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="378a7-145">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="378a7-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="378a7-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="378a7-146">Requirements</span></span>



| <span data-ttu-id="378a7-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="378a7-147">Requirement</span></span> | <span data-ttu-id="378a7-148">Valor</span><span class="sxs-lookup"><span data-stu-id="378a7-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="378a7-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378a7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="378a7-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="378a7-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="378a7-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378a7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="378a7-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="378a7-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="378a7-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="378a7-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="378a7-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378a7-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="378a7-155">DLL</span><span class="sxs-lookup"><span data-stu-id="378a7-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="378a7-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378a7-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="378a7-157">IID</span><span class="sxs-lookup"><span data-stu-id="378a7-157">IID</span></span><br/>                      | <span data-ttu-id="378a7-158">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="378a7-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="378a7-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="378a7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378a7-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="378a7-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="378a7-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="378a7-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="378a7-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="378a7-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="378a7-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="378a7-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="378a7-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="378a7-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="378a7-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="378a7-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="378a7-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="378a7-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="378a7-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="378a7-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="378a7-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="378a7-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="378a7-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="378a7-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





