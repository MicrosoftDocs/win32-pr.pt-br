---
title: Propriedade IMsTscAx HorizontalScrollBarVisible
description: Indica se o controle exibiu uma barra de rolagem horizontal.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009294"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="7b65a-124">Propriedade IMsTscAx:: HorizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="7b65a-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="7b65a-125">Indica se o controle exibiu uma barra de rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="7b65a-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="7b65a-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7b65a-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b65a-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b65a-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="7b65a-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7b65a-128">Property value</span></span>

<span data-ttu-id="7b65a-129">O valor desse parâmetro será **true** se a barra de rolagem horizontal estiver visível e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7b65a-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b65a-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7b65a-130">Error codes</span></span>

<span data-ttu-id="7b65a-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7b65a-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b65a-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b65a-132">Remarks</span></span>

<span data-ttu-id="7b65a-133">O controle exibirá automaticamente uma barra de rolagem horizontal se a largura do controle for menor que a largura da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7b65a-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="7b65a-134">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7b65a-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b65a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b65a-135">Requirements</span></span>



| <span data-ttu-id="7b65a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b65a-136">Requirement</span></span> | <span data-ttu-id="7b65a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="7b65a-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b65a-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b65a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7b65a-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b65a-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b65a-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b65a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7b65a-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b65a-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b65a-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7b65a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b65a-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b65a-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b65a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7b65a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b65a-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b65a-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b65a-146">IID</span><span class="sxs-lookup"><span data-stu-id="7b65a-146">IID</span></span><br/>                      | <span data-ttu-id="7b65a-147">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="7b65a-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7b65a-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b65a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b65a-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="7b65a-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="7b65a-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="7b65a-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="7b65a-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="7b65a-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="7b65a-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="7b65a-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="7b65a-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="7b65a-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="7b65a-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="7b65a-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="7b65a-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7b65a-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7b65a-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7b65a-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7b65a-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7b65a-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7b65a-158">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="7b65a-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="7b65a-159">**VerticalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="7b65a-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





