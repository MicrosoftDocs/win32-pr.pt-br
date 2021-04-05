---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyAltSpace
description: Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + espaço.
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyAltSpace
- Propriedade HotKeyAltSpace Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyAltSpace
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b257bd04171f8bff22bbe91ee7310fafe89c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918370"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a><span data-ttu-id="4b24b-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyAltSpace</span><span class="sxs-lookup"><span data-stu-id="4b24b-120">IMsRdpClientAdvancedSettings::HotKeyAltSpace property</span></span>

<span data-ttu-id="4b24b-121">Especifica o código de chave virtual a ser adicionado a ALT para determinar a substituição de tecla de atalho para ALT + espaço.</span><span class="sxs-lookup"><span data-stu-id="4b24b-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SPACE.</span></span>

<span data-ttu-id="4b24b-122">Essa propriedade é válida somente quando a propriedade [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4b24b-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="4b24b-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4b24b-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b24b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b24b-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a><span data-ttu-id="4b24b-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4b24b-125">Property value</span></span>

<span data-ttu-id="4b24b-126">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="4b24b-126">The new virtual-key code.</span></span> <span data-ttu-id="4b24b-127">**VK \_ DELETE** é o padrão, com Alt + Delete como a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="4b24b-127">**VK\_DELETE** is the default, with ALT+DELETE as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b24b-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4b24b-128">Error codes</span></span>

<span data-ttu-id="4b24b-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4b24b-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b24b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b24b-130">Remarks</span></span>

<span data-ttu-id="4b24b-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4b24b-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b24b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b24b-132">Requirements</span></span>



| <span data-ttu-id="4b24b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b24b-133">Requirement</span></span> | <span data-ttu-id="4b24b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4b24b-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b24b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b24b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4b24b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b24b-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4b24b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b24b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4b24b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b24b-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4b24b-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4b24b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b24b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b24b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4b24b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4b24b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b24b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b24b-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4b24b-143">IID</span><span class="sxs-lookup"><span data-stu-id="4b24b-143">IID</span></span><br/>                      | <span data-ttu-id="4b24b-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4b24b-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b24b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b24b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b24b-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4b24b-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4b24b-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4b24b-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4b24b-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4b24b-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4b24b-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4b24b-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4b24b-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4b24b-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4b24b-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4b24b-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4b24b-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4b24b-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4b24b-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4b24b-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





