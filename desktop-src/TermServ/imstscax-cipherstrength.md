---
title: Propriedade IMsTscAx CipherStrength
description: Recupera a intensidade máxima de criptografia do controle atual.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, propriedade CipherStrength
- Propriedade CipherStrength Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, propriedade CipherStrength
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369303"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="94b4b-124">Propriedade IMsTscAx:: CipherStrength</span><span class="sxs-lookup"><span data-stu-id="94b4b-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="94b4b-125">Recupera a intensidade máxima de criptografia do controle atual.</span><span class="sxs-lookup"><span data-stu-id="94b4b-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="94b4b-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="94b4b-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b4b-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94b4b-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="94b4b-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="94b4b-128">Property value</span></span>

<span data-ttu-id="94b4b-129">O nível de criptografia.</span><span class="sxs-lookup"><span data-stu-id="94b4b-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="94b4b-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="94b4b-130">Error codes</span></span>

<span data-ttu-id="94b4b-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="94b4b-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b4b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="94b4b-132">Remarks</span></span>

<span data-ttu-id="94b4b-133">Por Conexão Web de Área de Trabalho Remota, a intensidade de codificação é sempre 128 porque o controle ActiveX Área de Trabalho Remota dá suporte à criptografia até e incluindo 128 bits.</span><span class="sxs-lookup"><span data-stu-id="94b4b-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="94b4b-134">O controle de 128 bits ainda pode se conectar a servidores de Host da Sessão da Área de Trabalho Remota de criptografia de 56 bits (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="94b4b-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="94b4b-135">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="94b4b-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94b4b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b4b-136">Requirements</span></span>



| <span data-ttu-id="94b4b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b4b-137">Requirement</span></span> | <span data-ttu-id="94b4b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="94b4b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b4b-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94b4b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="94b4b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94b4b-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="94b4b-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94b4b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="94b4b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94b4b-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="94b4b-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="94b4b-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="94b4b-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b4b-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="94b4b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="94b4b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b4b-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b4b-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="94b4b-147">IID</span><span class="sxs-lookup"><span data-stu-id="94b4b-147">IID</span></span><br/>                      | <span data-ttu-id="94b4b-148">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="94b4b-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="94b4b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="94b4b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b4b-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="94b4b-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="94b4b-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="94b4b-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="94b4b-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="94b4b-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="94b4b-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="94b4b-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="94b4b-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="94b4b-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="94b4b-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="94b4b-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="94b4b-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="94b4b-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="94b4b-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="94b4b-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="94b4b-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="94b4b-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="94b4b-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="94b4b-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





