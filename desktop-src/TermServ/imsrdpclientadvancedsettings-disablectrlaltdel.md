---
title: Propriedade IMsRdpClientAdvancedSettings DisableCtrlAltDel
description: Especifica se a tela de explicação inicial no Winlogon deve ser exibida.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade DisableCtrlAltDel
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade DisableCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644414"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="ea7df-120">IMsRdpClientAdvancedSettings: Propriedade isableCtrlAltDel de:D</span><span class="sxs-lookup"><span data-stu-id="ea7df-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="ea7df-121">Especifica se a tela de explicação inicial no Winlogon deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="ea7df-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="ea7df-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ea7df-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea7df-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea7df-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="ea7df-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ea7df-124">Property value</span></span>

<span data-ttu-id="ea7df-125">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="ea7df-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ea7df-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ea7df-126">Error codes</span></span>

<span data-ttu-id="ea7df-127">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ea7df-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea7df-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea7df-128">Remarks</span></span>

<span data-ttu-id="ea7df-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ea7df-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea7df-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea7df-130">Requirements</span></span>



| <span data-ttu-id="ea7df-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea7df-131">Requirement</span></span> | <span data-ttu-id="ea7df-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ea7df-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7df-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea7df-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ea7df-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea7df-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ea7df-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea7df-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ea7df-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea7df-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ea7df-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ea7df-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea7df-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea7df-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ea7df-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ea7df-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea7df-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea7df-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ea7df-141">IID</span><span class="sxs-lookup"><span data-stu-id="ea7df-141">IID</span></span><br/>                      | <span data-ttu-id="ea7df-142">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ea7df-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea7df-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea7df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea7df-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ea7df-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ea7df-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ea7df-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ea7df-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ea7df-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ea7df-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ea7df-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ea7df-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ea7df-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ea7df-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ea7df-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ea7df-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ea7df-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ea7df-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ea7df-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





