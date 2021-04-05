---
title: Propriedade IMsTscAx AdvancedSettings
description: Recupera um ponteiro de interface IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918441"
---
# <a name="imstscaxadvancedsettings-property"></a><span data-ttu-id="adeae-124">Propriedade IMsTscAx:: AdvancedSettings</span><span class="sxs-lookup"><span data-stu-id="adeae-124">IMsTscAx::AdvancedSettings property</span></span>

<span data-ttu-id="adeae-125">Recupera um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="adeae-125">Retrieves an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="adeae-126">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="adeae-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="adeae-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adeae-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="adeae-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="adeae-128">Property value</span></span>

<span data-ttu-id="adeae-129">Um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="adeae-129">An [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="adeae-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="adeae-130">Error codes</span></span>

<span data-ttu-id="adeae-131">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="adeae-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="adeae-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="adeae-132">Remarks</span></span>

<span data-ttu-id="adeae-133">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="adeae-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adeae-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adeae-134">Requirements</span></span>



| <span data-ttu-id="adeae-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="adeae-135">Requirement</span></span> | <span data-ttu-id="adeae-136">Valor</span><span class="sxs-lookup"><span data-stu-id="adeae-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adeae-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adeae-137">Minimum supported client</span></span><br/> | <span data-ttu-id="adeae-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adeae-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="adeae-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adeae-139">Minimum supported server</span></span><br/> | <span data-ttu-id="adeae-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adeae-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="adeae-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="adeae-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="adeae-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adeae-142"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="adeae-143">DLL</span><span class="sxs-lookup"><span data-stu-id="adeae-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adeae-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adeae-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="adeae-145">IID</span><span class="sxs-lookup"><span data-stu-id="adeae-145">IID</span></span><br/>                      | <span data-ttu-id="adeae-146">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="adeae-146">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="adeae-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="adeae-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adeae-148">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="adeae-148">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="adeae-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="adeae-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="adeae-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="adeae-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="adeae-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="adeae-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="adeae-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="adeae-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="adeae-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="adeae-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="adeae-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="adeae-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="adeae-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="adeae-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="adeae-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="adeae-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="adeae-157">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="adeae-157">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





