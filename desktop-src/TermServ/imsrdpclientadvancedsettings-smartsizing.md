---
title: Propriedade IMsRdpClientAdvancedSettings SmartSizing
description: Especifica se a exibição deve ser dimensionada para se ajustar à área do cliente do controle. Observe que as barras de rolagem não aparecem quando a propriedade SmartSizing está habilitada.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade SmartSizing
- Propriedade SmartSizing Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade SmartSizing
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369232"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="635b1-121">Propriedade IMsRdpClientAdvancedSettings:: SmartSizing</span><span class="sxs-lookup"><span data-stu-id="635b1-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="635b1-122">Especifica se a exibição deve ser dimensionada para se ajustar à área do cliente do controle.</span><span class="sxs-lookup"><span data-stu-id="635b1-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="635b1-123">Observe que as barras de rolagem não aparecem quando a propriedade **SmartSizing** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="635b1-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="635b1-124">Ao contrário da maioria das outras propriedades, essa propriedade pode ser definida quando o controle é conectado.</span><span class="sxs-lookup"><span data-stu-id="635b1-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="635b1-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="635b1-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="635b1-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="635b1-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="635b1-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="635b1-127">Property value</span></span>

<span data-ttu-id="635b1-128">Defina esse parâmetro como **Variant \_ false** para desabilitar o recurso ou a **variante \_ true** para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="635b1-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="635b1-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="635b1-129">Error codes</span></span>

<span data-ttu-id="635b1-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="635b1-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="635b1-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="635b1-131">Remarks</span></span>

<span data-ttu-id="635b1-132">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="635b1-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="635b1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="635b1-133">Requirements</span></span>



| <span data-ttu-id="635b1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="635b1-134">Requirement</span></span> | <span data-ttu-id="635b1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="635b1-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="635b1-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="635b1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="635b1-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="635b1-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="635b1-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="635b1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="635b1-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="635b1-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="635b1-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="635b1-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="635b1-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="635b1-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="635b1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="635b1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="635b1-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="635b1-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="635b1-144">IID</span><span class="sxs-lookup"><span data-stu-id="635b1-144">IID</span></span><br/>                      | <span data-ttu-id="635b1-145">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="635b1-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="635b1-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="635b1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635b1-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="635b1-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="635b1-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="635b1-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="635b1-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="635b1-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="635b1-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="635b1-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="635b1-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="635b1-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="635b1-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="635b1-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="635b1-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="635b1-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="635b1-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="635b1-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





