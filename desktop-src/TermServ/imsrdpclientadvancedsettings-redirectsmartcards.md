---
title: Propriedade IMsRdpClientAdvancedSettings RedirectSmartCards
description: Especifica se o redirecionamento de cartões inteligentes é permitido.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectSmartCards
- Propriedade RedirectSmartCards Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectSmartCards
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756970"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a><span data-ttu-id="e90ef-120">Propriedade IMsRdpClientAdvancedSettings:: RedirectSmartCards</span><span class="sxs-lookup"><span data-stu-id="e90ef-120">IMsRdpClientAdvancedSettings::RedirectSmartCards property</span></span>

<span data-ttu-id="e90ef-121">Especifica se o redirecionamento de cartões inteligentes é permitido.</span><span class="sxs-lookup"><span data-stu-id="e90ef-121">Specifies if redirection of smart cards is allowed.</span></span>

<span data-ttu-id="e90ef-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e90ef-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90ef-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e90ef-123">Syntax</span></span>


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a><span data-ttu-id="e90ef-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e90ef-124">Property value</span></span>

<span data-ttu-id="e90ef-125">Defina esse parâmetro como **Variant \_ true** para permitir redirecionamento ou **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e90ef-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="e90ef-126">**Variante \_ VERDADEIRO** solicita que o usuário confirme a permissão de redirecionamento no momento da conexão, para fins de segurança.</span><span class="sxs-lookup"><span data-stu-id="e90ef-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e90ef-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e90ef-127">Error codes</span></span>

<span data-ttu-id="e90ef-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e90ef-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e90ef-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="e90ef-129">Remarks</span></span>

<span data-ttu-id="e90ef-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e90ef-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e90ef-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e90ef-131">Requirements</span></span>



| <span data-ttu-id="e90ef-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90ef-132">Requirement</span></span> | <span data-ttu-id="e90ef-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e90ef-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90ef-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e90ef-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e90ef-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e90ef-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e90ef-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e90ef-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e90ef-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e90ef-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e90ef-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e90ef-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e90ef-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90ef-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e90ef-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e90ef-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90ef-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90ef-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e90ef-142">IID</span><span class="sxs-lookup"><span data-stu-id="e90ef-142">IID</span></span><br/>                      | <span data-ttu-id="e90ef-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e90ef-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e90ef-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e90ef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90ef-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e90ef-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e90ef-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e90ef-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e90ef-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e90ef-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e90ef-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e90ef-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e90ef-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e90ef-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e90ef-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e90ef-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e90ef-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e90ef-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e90ef-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e90ef-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





