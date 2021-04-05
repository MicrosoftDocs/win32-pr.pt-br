---
title: Propriedade IMsRdpClient ColorDepth
description: A profundidade de cor (em bits por pixel) para a conexão do controle.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade ColorDepth
- Propriedade ColorDepth Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade ColorDepth
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086288"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="18e30-124">Propriedade IMsRdpClient:: ColorDepth</span><span class="sxs-lookup"><span data-stu-id="18e30-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="18e30-125">A profundidade de cor (em bits por pixel) para a conexão do controle.</span><span class="sxs-lookup"><span data-stu-id="18e30-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="18e30-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="18e30-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e30-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="18e30-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="18e30-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="18e30-128">Property value</span></span>

<span data-ttu-id="18e30-129">A intensidade da cor.</span><span class="sxs-lookup"><span data-stu-id="18e30-129">The color depth.</span></span> <span data-ttu-id="18e30-130">Os valores incluem 8, 15, 16, 24 e 32 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="18e30-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18e30-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="18e30-131">Error codes</span></span>

<span data-ttu-id="18e30-132">Se os métodos forem bem-sucedidos, será retornado **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="18e30-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="18e30-133">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="18e30-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="18e30-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="18e30-134">Remarks</span></span>

<span data-ttu-id="18e30-135">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="18e30-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="18e30-136">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="18e30-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18e30-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e30-137">Requirements</span></span>



| <span data-ttu-id="18e30-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e30-138">Requirement</span></span> | <span data-ttu-id="18e30-139">Valor</span><span class="sxs-lookup"><span data-stu-id="18e30-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18e30-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18e30-140">Minimum supported client</span></span><br/> | <span data-ttu-id="18e30-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18e30-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="18e30-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18e30-142">Minimum supported server</span></span><br/> | <span data-ttu-id="18e30-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18e30-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="18e30-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="18e30-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="18e30-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="18e30-146">DLL</span><span class="sxs-lookup"><span data-stu-id="18e30-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e30-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="18e30-148">IID</span><span class="sxs-lookup"><span data-stu-id="18e30-148">IID</span></span><br/>                      | <span data-ttu-id="18e30-149">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="18e30-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="18e30-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="18e30-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e30-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="18e30-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="18e30-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="18e30-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="18e30-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="18e30-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="18e30-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="18e30-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="18e30-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="18e30-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="18e30-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="18e30-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="18e30-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="18e30-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="18e30-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="18e30-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="18e30-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="18e30-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="18e30-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="18e30-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





