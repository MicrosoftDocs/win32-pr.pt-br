---
title: Propriedade IMsRdpClientAdvancedSettings NumBitmapCaches
description: Não há suporte a esta propriedade. | Propriedade IMsRdpClientAdvancedSettings NumBitmapCaches
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade NumBitmapCaches
- Propriedade NumBitmapCaches Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade NumBitmapCaches
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105789831"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a><span data-ttu-id="d4d9a-121">Propriedade IMsRdpClientAdvancedSettings:: NumBitmapCaches</span><span class="sxs-lookup"><span data-stu-id="d4d9a-121">IMsRdpClientAdvancedSettings::NumBitmapCaches property</span></span>

<span data-ttu-id="d4d9a-122">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="d4d9a-122">This property is not supported.</span></span>

<span data-ttu-id="d4d9a-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d4d9a-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d9a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4d9a-124">Syntax</span></span>


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a><span data-ttu-id="d4d9a-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d4d9a-125">Property value</span></span>

<span data-ttu-id="d4d9a-126">O novo número de caches.</span><span class="sxs-lookup"><span data-stu-id="d4d9a-126">The new number of caches.</span></span> <span data-ttu-id="d4d9a-127">O valor padrão é 3, o que resulta no melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="d4d9a-127">The default value is 3, which results in the best performance.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4d9a-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d4d9a-128">Error codes</span></span>

<span data-ttu-id="d4d9a-129">Retorna **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d4d9a-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d9a-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4d9a-130">Remarks</span></span>

<span data-ttu-id="d4d9a-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d4d9a-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d9a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4d9a-132">Requirements</span></span>



| <span data-ttu-id="d4d9a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d9a-133">Requirement</span></span> | <span data-ttu-id="d4d9a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d4d9a-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d9a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4d9a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d9a-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4d9a-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4d9a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4d9a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d9a-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4d9a-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4d9a-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d4d9a-139">End of client support</span></span><br/>    | <span data-ttu-id="d4d9a-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4d9a-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4d9a-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d4d9a-141">End of server support</span></span><br/>    | <span data-ttu-id="d4d9a-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4d9a-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4d9a-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d4d9a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4d9a-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d9a-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d4d9a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d4d9a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d9a-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d9a-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d4d9a-147">IID</span><span class="sxs-lookup"><span data-stu-id="d4d9a-147">IID</span></span><br/>                      | <span data-ttu-id="d4d9a-148">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d4d9a-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4d9a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4d9a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d9a-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d4d9a-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d4d9a-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





