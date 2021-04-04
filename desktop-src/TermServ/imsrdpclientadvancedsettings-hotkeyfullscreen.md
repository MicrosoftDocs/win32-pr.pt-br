---
title: Propriedade IMsRdpClientAdvancedSettings HotKeyFullScreen
description: Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para alternar para o modo de tela inteira.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyFullScreen
- Propriedade HotKeyFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918074"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="bbca7-120">Propriedade IMsRdpClientAdvancedSettings:: HotKeyFullScreen</span><span class="sxs-lookup"><span data-stu-id="bbca7-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="bbca7-121">Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para alternar para o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="bbca7-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="bbca7-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bbca7-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbca7-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbca7-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="bbca7-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bbca7-124">Property value</span></span>

<span data-ttu-id="bbca7-125">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="bbca7-125">The new virtual-key code.</span></span> <span data-ttu-id="bbca7-126">**VK \_ CANCEL** é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="bbca7-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bbca7-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bbca7-127">Error codes</span></span>

<span data-ttu-id="bbca7-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bbca7-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbca7-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbca7-129">Remarks</span></span>

<span data-ttu-id="bbca7-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bbca7-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbca7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbca7-131">Requirements</span></span>



| <span data-ttu-id="bbca7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbca7-132">Requirement</span></span> | <span data-ttu-id="bbca7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="bbca7-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbca7-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbca7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bbca7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbca7-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="bbca7-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbca7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bbca7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbca7-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="bbca7-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bbca7-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbca7-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbca7-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bbca7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bbca7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbca7-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbca7-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bbca7-142">IID</span><span class="sxs-lookup"><span data-stu-id="bbca7-142">IID</span></span><br/>                      | <span data-ttu-id="bbca7-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="bbca7-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbca7-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbca7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbca7-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bbca7-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bbca7-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bbca7-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bbca7-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bbca7-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bbca7-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bbca7-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bbca7-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bbca7-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bbca7-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bbca7-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bbca7-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bbca7-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bbca7-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bbca7-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





