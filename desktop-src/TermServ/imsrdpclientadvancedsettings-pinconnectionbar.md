---
title: Propriedade IMsRdpClientAdvancedSettings PinConnectionBar
description: Especifica o estado da barra de conexão da interface do usuário.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade PinConnectionBar
- Propriedade PinConnectionBar Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade PinConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824178"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="d3afe-120">IMsRdpClientAdvancedSettings: Propriedade inConnectionBar de:P</span><span class="sxs-lookup"><span data-stu-id="d3afe-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="d3afe-121">Especifica o estado da barra de conexão da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d3afe-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="d3afe-122">Essa propriedade retornará **E \_ NOTIMPL** se o contêiner chamar o método [**IObjectSafety:: SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d3afe-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="d3afe-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d3afe-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3afe-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3afe-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="d3afe-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d3afe-125">Property value</span></span>

<span data-ttu-id="d3afe-126">Definir essa propriedade como **Variant \_ true** define o estado como "diminuído", ou seja, invisível para o usuário e indisponível para entrada.</span><span class="sxs-lookup"><span data-stu-id="d3afe-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="d3afe-127">**Variante \_ FALSE** define o estado como "disparado" e está disponível para entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="d3afe-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3afe-128">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d3afe-128">Error codes</span></span>

<span data-ttu-id="d3afe-129">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d3afe-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3afe-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3afe-130">Remarks</span></span>

<span data-ttu-id="d3afe-131">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d3afe-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3afe-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3afe-132">Requirements</span></span>



| <span data-ttu-id="d3afe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3afe-133">Requirement</span></span> | <span data-ttu-id="d3afe-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d3afe-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3afe-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3afe-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d3afe-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3afe-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d3afe-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3afe-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d3afe-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3afe-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d3afe-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d3afe-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3afe-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3afe-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d3afe-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d3afe-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3afe-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3afe-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d3afe-143">IID</span><span class="sxs-lookup"><span data-stu-id="d3afe-143">IID</span></span><br/>                      | <span data-ttu-id="d3afe-144">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d3afe-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3afe-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d3afe-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3afe-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d3afe-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d3afe-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d3afe-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d3afe-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d3afe-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d3afe-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d3afe-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d3afe-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d3afe-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d3afe-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d3afe-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d3afe-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d3afe-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d3afe-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d3afe-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

