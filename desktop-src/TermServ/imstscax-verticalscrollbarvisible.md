---
title: Propriedade IMsTscAx VerticalScrollBarVisible
description: Indica se o controle exibe uma barra de rolagem vertical.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454833"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="cfc9e-124">Propriedade IMsTscAx:: VerticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="cfc9e-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="cfc9e-125">Indica se o controle exibe uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="cfc9e-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="cfc9e-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="cfc9e-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc9e-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfc9e-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="cfc9e-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cfc9e-128">Property value</span></span>

<span data-ttu-id="cfc9e-129">O valor desse parâmetro será **true** se a barra de rolagem vertical estiver visível e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cfc9e-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cfc9e-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cfc9e-130">Error codes</span></span>

<span data-ttu-id="cfc9e-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cfc9e-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc9e-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfc9e-132">Remarks</span></span>

<span data-ttu-id="cfc9e-133">O controle exibirá automaticamente uma barra de rolagem vertical se a altura do controle atual for menor que a altura da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cfc9e-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="cfc9e-134">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cfc9e-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc9e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfc9e-135">Requirements</span></span>



| <span data-ttu-id="cfc9e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc9e-136">Requirement</span></span> | <span data-ttu-id="cfc9e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="cfc9e-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc9e-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfc9e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc9e-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfc9e-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cfc9e-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfc9e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc9e-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfc9e-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cfc9e-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cfc9e-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfc9e-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc9e-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cfc9e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cfc9e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfc9e-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc9e-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cfc9e-146">IID</span><span class="sxs-lookup"><span data-stu-id="cfc9e-146">IID</span></span><br/>                      | <span data-ttu-id="cfc9e-147">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="cfc9e-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="cfc9e-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfc9e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc9e-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-158">**HorizontalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="cfc9e-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="cfc9e-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





