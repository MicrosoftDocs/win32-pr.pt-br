---
title: Propriedade IMsTscAx DesktopHeight
description: Especifica a altura do controle atual, em pixels, na área de trabalho remota inicial.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade DesktopHeight
- Propriedade DesktopHeight Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade DesktopHeight
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918734"
---
# <a name="imstscaxdesktopheight-property"></a><span data-ttu-id="84495-124">IMsTscAx: Propriedade esktopHeight de:D</span><span class="sxs-lookup"><span data-stu-id="84495-124">IMsTscAx::DesktopHeight property</span></span>

<span data-ttu-id="84495-125">Especifica a altura do controle atual, em pixels, na área de trabalho remota inicial.</span><span class="sxs-lookup"><span data-stu-id="84495-125">Specifies the current control's height, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="84495-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="84495-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="84495-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="84495-127">Syntax</span></span>


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="84495-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="84495-128">Property value</span></span>

<span data-ttu-id="84495-129">A nova altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="84495-129">The new height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84495-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="84495-130">Error codes</span></span>

<span data-ttu-id="84495-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="84495-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="84495-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="84495-132">Remarks</span></span>

<span data-ttu-id="84495-133">A definição da propriedade **DesktopHeight** é opcional, mas deve ser definida antes de chamar o método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="84495-133">Setting the **DesktopHeight** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="84495-134">Se uma altura da área de trabalho não for especificada ou for definida como zero, a altura da área de trabalho será definida como a altura do controle.</span><span class="sxs-lookup"><span data-stu-id="84495-134">If a desktop height is not specified, or is set to zero, the desktop height is set to the height of the control.</span></span> <span data-ttu-id="84495-135">Os valores mínimo e máximo dependem da versão do sistema operacional do cliente de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="84495-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="84495-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84495-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="84495-137">mínimo de 200, 8192 máximo</span><span class="sxs-lookup"><span data-stu-id="84495-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="84495-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84495-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="84495-139">mínimo de 200, 2048 máximo</span><span class="sxs-lookup"><span data-stu-id="84495-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="84495-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84495-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="84495-141">mínimo de 200, 1200 máximo</span><span class="sxs-lookup"><span data-stu-id="84495-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="84495-142">Depois que uma conexão é estabelecida, as alterações feitas na altura do controle não alteram a altura da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="84495-142">After a connection is established, any changes to the control's height do not change the height of the remote desktop.</span></span> <span data-ttu-id="84495-143">Em vez disso, o controle abre as barras de rolagem ou centraliza a área de trabalho remota, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="84495-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="84495-144">Para alterar o tamanho da área de trabalho de uma conexão ativa, use o método [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="84495-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="84495-145">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="84495-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84495-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84495-146">Requirements</span></span>



| <span data-ttu-id="84495-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="84495-147">Requirement</span></span> | <span data-ttu-id="84495-148">Valor</span><span class="sxs-lookup"><span data-stu-id="84495-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84495-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84495-149">Minimum supported client</span></span><br/> | <span data-ttu-id="84495-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84495-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="84495-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84495-151">Minimum supported server</span></span><br/> | <span data-ttu-id="84495-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84495-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="84495-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="84495-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="84495-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84495-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="84495-155">DLL</span><span class="sxs-lookup"><span data-stu-id="84495-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84495-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84495-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="84495-157">IID</span><span class="sxs-lookup"><span data-stu-id="84495-157">IID</span></span><br/>                      | <span data-ttu-id="84495-158">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="84495-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="84495-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="84495-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84495-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="84495-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="84495-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="84495-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="84495-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="84495-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="84495-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="84495-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="84495-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="84495-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="84495-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="84495-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="84495-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="84495-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="84495-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="84495-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="84495-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="84495-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="84495-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="84495-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





