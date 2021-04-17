---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyAltShiftTab
description: Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + SHIFT + TAB.
ms.assetid: da52f2fb-15cc-4d55-b26e-cf5465290889
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyAltShiftTab
- Propriedade HotKeyAltShiftTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyAltShiftTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltShiftTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819ddcba3f9cb10450525467eb8accce958c2f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783340"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltshifttab-property"></a><span data-ttu-id="51f35-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyAltShiftTab</span><span class="sxs-lookup"><span data-stu-id="51f35-120">IMsRdpClientAdvancedSettings::HotKeyAltShiftTab property</span></span>

<span data-ttu-id="51f35-121">Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + SHIFT + TAB.</span><span class="sxs-lookup"><span data-stu-id="51f35-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SHIFT+TAB.</span></span>

<span data-ttu-id="51f35-122">Essa propriedade é válida somente quando a propriedade [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="51f35-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="51f35-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="51f35-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f35-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="51f35-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltShiftTab(
  [in]  LONG hotKeyAltShiftTab
);

HRESULT get_HotKeyAltShiftTab(
  [out] LONG *photKeyAltShiftTab
);
```



## <a name="property-value"></a><span data-ttu-id="51f35-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="51f35-125">Property value</span></span>

<span data-ttu-id="51f35-126">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="51f35-126">The new virtual-key code.</span></span> <span data-ttu-id="51f35-127">**VK \_ Em seguida** , é o valor padrão, com Alt + Page Down como a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="51f35-127">**VK\_NEXT** is the default value, with ALT+PAGE DOWN as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="51f35-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="51f35-128">Error codes</span></span>

<span data-ttu-id="51f35-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="51f35-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f35-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="51f35-130">Remarks</span></span>

<span data-ttu-id="51f35-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="51f35-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51f35-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f35-132">Requirements</span></span>



| <span data-ttu-id="51f35-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f35-133">Requirement</span></span> | <span data-ttu-id="51f35-134">Valor</span><span class="sxs-lookup"><span data-stu-id="51f35-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f35-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51f35-135">Minimum supported client</span></span><br/> | <span data-ttu-id="51f35-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51f35-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="51f35-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51f35-137">Minimum supported server</span></span><br/> | <span data-ttu-id="51f35-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51f35-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="51f35-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="51f35-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="51f35-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51f35-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="51f35-141">DLL</span><span class="sxs-lookup"><span data-stu-id="51f35-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51f35-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51f35-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="51f35-143">IID</span><span class="sxs-lookup"><span data-stu-id="51f35-143">IID</span></span><br/>                      | <span data-ttu-id="51f35-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="51f35-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51f35-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="51f35-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f35-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="51f35-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="51f35-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="51f35-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="51f35-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="51f35-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="51f35-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="51f35-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="51f35-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="51f35-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="51f35-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="51f35-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="51f35-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="51f35-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="51f35-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="51f35-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





