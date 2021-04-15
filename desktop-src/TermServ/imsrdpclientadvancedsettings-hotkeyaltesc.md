---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyAltEsc
description: Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + ESC.
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyAltEsc
- Propriedade HotKeyAltEsc Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyAltEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b661a91a0204177525063629825c478b40b4c29e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456007"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a><span data-ttu-id="0ebf2-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyAltEsc</span><span class="sxs-lookup"><span data-stu-id="0ebf2-120">IMsRdpClientAdvancedSettings::HotKeyAltEsc property</span></span>

<span data-ttu-id="0ebf2-121">Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + ESC.</span><span class="sxs-lookup"><span data-stu-id="0ebf2-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+ESC.</span></span>

<span data-ttu-id="0ebf2-122">Essa propriedade é válida somente quando a propriedade [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0ebf2-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="0ebf2-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0ebf2-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebf2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ebf2-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a><span data-ttu-id="0ebf2-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0ebf2-125">Property value</span></span>

<span data-ttu-id="0ebf2-126">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="0ebf2-126">The new virtual-key code.</span></span> <span data-ttu-id="0ebf2-127">**VK \_ INSERT** é o valor padrão, com Alt + Insert como a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="0ebf2-127">**VK\_INSERT** is the default value, with ALT+INSERT as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0ebf2-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0ebf2-128">Error codes</span></span>

<span data-ttu-id="0ebf2-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0ebf2-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ebf2-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ebf2-130">Remarks</span></span>

<span data-ttu-id="0ebf2-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0ebf2-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebf2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebf2-132">Requirements</span></span>



| <span data-ttu-id="0ebf2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebf2-133">Requirement</span></span> | <span data-ttu-id="0ebf2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0ebf2-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebf2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ebf2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebf2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ebf2-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0ebf2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ebf2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebf2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ebf2-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0ebf2-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0ebf2-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ebf2-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ebf2-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0ebf2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0ebf2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ebf2-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ebf2-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0ebf2-143">IID</span><span class="sxs-lookup"><span data-stu-id="0ebf2-143">IID</span></span><br/>                      | <span data-ttu-id="0ebf2-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0ebf2-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ebf2-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ebf2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebf2-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0ebf2-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0ebf2-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





