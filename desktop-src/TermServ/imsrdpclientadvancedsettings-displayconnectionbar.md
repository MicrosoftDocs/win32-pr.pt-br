---
title: Propriedade IMsRdpClientAdvancedSettings DisplayConnectionBar
description: Especifica se a barra de conexão deve ser usada. O valor padrão é VARIANT \_ true, que habilita a propriedade.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade DisplayConnectionBar
- Propriedade DisplayConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade DisplayConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796300"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a><span data-ttu-id="bab82-121">IMsRdpClientAdvancedSettings: Propriedade isplayConnectionBar de:D</span><span class="sxs-lookup"><span data-stu-id="bab82-121">IMsRdpClientAdvancedSettings::DisplayConnectionBar property</span></span>

<span data-ttu-id="bab82-122">Especifica se a barra de conexão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="bab82-122">Specifies whether to use the connection bar.</span></span> <span data-ttu-id="bab82-123">O valor padrão é **Variant \_ true**, que habilita a propriedade.</span><span class="sxs-lookup"><span data-stu-id="bab82-123">The default value is **VARIANT\_TRUE**, which enables the property.</span></span> <span data-ttu-id="bab82-124">Definir essa propriedade como **Variant \_ false** em um ambiente de script seguro retorna **E \_ falha**.</span><span class="sxs-lookup"><span data-stu-id="bab82-124">Setting this property to **VARIANT\_FALSE** in a safe scripting environment returns **E\_FAIL**.</span></span>

<span data-ttu-id="bab82-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bab82-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab82-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab82-126">Syntax</span></span>


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="bab82-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bab82-127">Property value</span></span>

<span data-ttu-id="bab82-128">Defina esse parâmetro como **Variant \_ false** para desabilitar o recurso ou a **variante \_ true** para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="bab82-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="bab82-129">O valor padrão é **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="bab82-129">The default value is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bab82-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bab82-130">Error codes</span></span>

<span data-ttu-id="bab82-131">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bab82-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab82-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="bab82-132">Remarks</span></span>

<span data-ttu-id="bab82-133">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bab82-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bab82-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bab82-134">Requirements</span></span>



| <span data-ttu-id="bab82-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab82-135">Requirement</span></span> | <span data-ttu-id="bab82-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bab82-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab82-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab82-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bab82-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bab82-138">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="bab82-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab82-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bab82-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bab82-140">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="bab82-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bab82-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="bab82-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab82-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bab82-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bab82-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab82-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab82-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bab82-145">IID</span><span class="sxs-lookup"><span data-stu-id="bab82-145">IID</span></span><br/>                      | <span data-ttu-id="bab82-146">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="bab82-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bab82-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="bab82-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab82-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bab82-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bab82-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bab82-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bab82-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bab82-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bab82-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bab82-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bab82-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bab82-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bab82-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bab82-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bab82-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bab82-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bab82-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bab82-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





