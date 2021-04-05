---
title: Propriedade IMsRdpClientAdvancedSettings EnableWindowsKey
description: Especifica se a chave do Windows pode ser usada na sessão remota.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade EnableWindowsKey
- Propriedade EnableWindowsKey Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade EnableWindowsKey
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e31571e44d6b391250c32268750b25a76105eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645099"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a><span data-ttu-id="2d7cc-120">Propriedade IMsRdpClientAdvancedSettings:: EnableWindowsKey</span><span class="sxs-lookup"><span data-stu-id="2d7cc-120">IMsRdpClientAdvancedSettings::EnableWindowsKey property</span></span>

<span data-ttu-id="2d7cc-121">Especifica se a chave do Windows pode ser usada na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="2d7cc-121">Specifies if the Windows key can be used in the remote session.</span></span>

<span data-ttu-id="2d7cc-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2d7cc-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7cc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d7cc-123">Syntax</span></span>


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a><span data-ttu-id="2d7cc-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2d7cc-124">Property value</span></span>

<span data-ttu-id="2d7cc-125">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="2d7cc-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d7cc-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2d7cc-126">Error codes</span></span>

<span data-ttu-id="2d7cc-127">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2d7cc-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d7cc-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d7cc-128">Remarks</span></span>

<span data-ttu-id="2d7cc-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2d7cc-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d7cc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d7cc-130">Requirements</span></span>



| <span data-ttu-id="2d7cc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d7cc-131">Requirement</span></span> | <span data-ttu-id="2d7cc-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2d7cc-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7cc-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d7cc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2d7cc-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d7cc-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="2d7cc-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d7cc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2d7cc-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d7cc-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="2d7cc-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2d7cc-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d7cc-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d7cc-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2d7cc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2d7cc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d7cc-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d7cc-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2d7cc-141">IID</span><span class="sxs-lookup"><span data-stu-id="2d7cc-141">IID</span></span><br/>                      | <span data-ttu-id="2d7cc-142">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="2d7cc-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d7cc-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d7cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7cc-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2d7cc-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2d7cc-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





