---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyCtrlEsc
description: Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para CTRL + ESC.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyCtrlEsc
- Propriedade HotKeyCtrlEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyCtrlEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781023"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a><span data-ttu-id="15462-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyCtrlEsc</span><span class="sxs-lookup"><span data-stu-id="15462-120">IMsRdpClientAdvancedSettings::HotKeyCtrlEsc property</span></span>

<span data-ttu-id="15462-121">Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para CTRL + ESC.</span><span class="sxs-lookup"><span data-stu-id="15462-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for CTRL+ESC.</span></span>

<span data-ttu-id="15462-122">Essa propriedade é válida somente quando a propriedade [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="15462-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="15462-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="15462-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="15462-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="15462-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a><span data-ttu-id="15462-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="15462-125">Property value</span></span>

<span data-ttu-id="15462-126">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="15462-126">The new virtual-key code.</span></span> <span data-ttu-id="15462-127">**VK \_ HOME** é o valor padrão, com Alt + Home como a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="15462-127">**VK\_HOME** is the default value, with ALT+HOME as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="15462-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="15462-128">Error codes</span></span>

<span data-ttu-id="15462-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="15462-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="15462-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="15462-130">Remarks</span></span>

<span data-ttu-id="15462-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="15462-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15462-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15462-132">Requirements</span></span>



| <span data-ttu-id="15462-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="15462-133">Requirement</span></span> | <span data-ttu-id="15462-134">Valor</span><span class="sxs-lookup"><span data-stu-id="15462-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15462-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15462-135">Minimum supported client</span></span><br/> | <span data-ttu-id="15462-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15462-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="15462-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15462-137">Minimum supported server</span></span><br/> | <span data-ttu-id="15462-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15462-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="15462-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="15462-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="15462-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15462-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="15462-141">DLL</span><span class="sxs-lookup"><span data-stu-id="15462-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15462-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15462-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="15462-143">IID</span><span class="sxs-lookup"><span data-stu-id="15462-143">IID</span></span><br/>                      | <span data-ttu-id="15462-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="15462-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15462-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="15462-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15462-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="15462-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="15462-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="15462-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="15462-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="15462-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="15462-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="15462-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="15462-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="15462-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="15462-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="15462-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="15462-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="15462-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="15462-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="15462-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





