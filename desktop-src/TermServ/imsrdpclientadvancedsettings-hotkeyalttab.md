---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyAltTab
description: Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyAltTab
- Propriedade HotKeyAltTab Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369443"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a><span data-ttu-id="fa96b-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyAltTab</span><span class="sxs-lookup"><span data-stu-id="fa96b-120">IMsRdpClientAdvancedSettings::HotKeyAltTab property</span></span>

<span data-ttu-id="fa96b-121">Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="fa96b-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+TAB.</span></span>

<span data-ttu-id="fa96b-122">Essa propriedade é válida somente quando a propriedade [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fa96b-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="fa96b-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fa96b-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa96b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa96b-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a><span data-ttu-id="fa96b-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fa96b-125">Property value</span></span>

<span data-ttu-id="fa96b-126">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="fa96b-126">The new virtual-key code.</span></span> <span data-ttu-id="fa96b-127">**VK \_ ANTERIOR** é o valor padrão, com Alt + Page Up como a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="fa96b-127">**VK\_PRIOR** is the default value, with ALT+PAGE UP as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa96b-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fa96b-128">Error codes</span></span>

<span data-ttu-id="fa96b-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa96b-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa96b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa96b-130">Remarks</span></span>

<span data-ttu-id="fa96b-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fa96b-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa96b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa96b-132">Requirements</span></span>



| <span data-ttu-id="fa96b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa96b-133">Requirement</span></span> | <span data-ttu-id="fa96b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fa96b-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa96b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa96b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fa96b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa96b-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fa96b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa96b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fa96b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa96b-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fa96b-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fa96b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa96b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa96b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fa96b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fa96b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa96b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa96b-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fa96b-143">IID</span><span class="sxs-lookup"><span data-stu-id="fa96b-143">IID</span></span><br/>                      | <span data-ttu-id="fa96b-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fa96b-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa96b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa96b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa96b-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fa96b-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fa96b-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fa96b-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fa96b-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fa96b-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fa96b-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fa96b-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fa96b-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fa96b-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fa96b-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fa96b-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fa96b-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fa96b-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fa96b-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fa96b-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





