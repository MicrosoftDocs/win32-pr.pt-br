---
title: Propriedade IMsRdpClientAdvancedSettings RedirectPrinters
description: Especifica se o redirecionamento de impressoras é permitido.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectPrinters
- Propriedade RedirectPrinters Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectPrinters
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644280"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="7463f-120">Propriedade IMsRdpClientAdvancedSettings:: RedirectPrinters</span><span class="sxs-lookup"><span data-stu-id="7463f-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="7463f-121">Especifica se o redirecionamento de impressoras é permitido.</span><span class="sxs-lookup"><span data-stu-id="7463f-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="7463f-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7463f-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7463f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7463f-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="7463f-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7463f-124">Property value</span></span>

<span data-ttu-id="7463f-125">Defina esse parâmetro como **Variant \_ true** para permitir redirecionamento ou **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7463f-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7463f-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7463f-126">Error codes</span></span>

<span data-ttu-id="7463f-127">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7463f-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7463f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7463f-128">Remarks</span></span>

<span data-ttu-id="7463f-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7463f-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7463f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7463f-130">Requirements</span></span>



| <span data-ttu-id="7463f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7463f-131">Requirement</span></span> | <span data-ttu-id="7463f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7463f-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7463f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7463f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7463f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7463f-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="7463f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7463f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7463f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7463f-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="7463f-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7463f-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="7463f-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7463f-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7463f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7463f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7463f-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7463f-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7463f-141">IID</span><span class="sxs-lookup"><span data-stu-id="7463f-141">IID</span></span><br/>                      | <span data-ttu-id="7463f-142">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7463f-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7463f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7463f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7463f-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7463f-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7463f-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7463f-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7463f-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7463f-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7463f-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7463f-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7463f-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7463f-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7463f-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7463f-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7463f-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7463f-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7463f-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7463f-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





