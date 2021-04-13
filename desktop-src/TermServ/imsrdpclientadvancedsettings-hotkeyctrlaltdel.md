---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyCtrlAltDel
description: Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para CTRL + ALT + DELETE, também chamada de seqüência de atenção segura (SAS).
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyCtrlAltDel
- Propriedade HotKeyCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369307"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a><span data-ttu-id="7fbb4-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyCtrlAltDel</span><span class="sxs-lookup"><span data-stu-id="7fbb4-120">IMsRdpClientAdvancedSettings::HotKeyCtrlAltDel property</span></span>

<span data-ttu-id="7fbb4-121">Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para CTRL + ALT + DELETE, também chamada de seqüência de atenção segura (SAS).</span><span class="sxs-lookup"><span data-stu-id="7fbb4-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+DELETE, also called the secure attention sequence (SAS).</span></span>

> [!Note]  
> <span data-ttu-id="7fbb4-122">CTRL + ALT + DELETE nunca é redirecionado para o servidor remoto, mesmo quando a propriedade [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) está habilitada; CTRL + ALT + DELETE é a sequência SAS local.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-122">CTRL+ALT+DELETE is never redirected to the remote server, even when the [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) property is enabled; CTRL+ALT+DELETE is the local SAS sequence.</span></span>

 

<span data-ttu-id="7fbb4-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbb4-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fbb4-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="7fbb4-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbb4-125">Property value</span></span>

<span data-ttu-id="7fbb4-126">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-126">The new virtual-key code.</span></span> <span data-ttu-id="7fbb4-127">**VK \_ END** é o padrão.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-127">**VK\_END** is the default.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7fbb4-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7fbb4-128">Error codes</span></span>

<span data-ttu-id="7fbb4-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbb4-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fbb4-130">Remarks</span></span>

<span data-ttu-id="7fbb4-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7fbb4-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbb4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbb4-132">Requirements</span></span>



| <span data-ttu-id="7fbb4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbb4-133">Requirement</span></span> | <span data-ttu-id="7fbb4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbb4-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbb4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fbb4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbb4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fbb4-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="7fbb4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fbb4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbb4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fbb4-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="7fbb4-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7fbb4-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="7fbb4-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbb4-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7fbb4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7fbb4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fbb4-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbb4-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7fbb4-143">IID</span><span class="sxs-lookup"><span data-stu-id="7fbb4-143">IID</span></span><br/>                      | <span data-ttu-id="7fbb4-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7fbb4-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7fbb4-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fbb4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbb4-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





