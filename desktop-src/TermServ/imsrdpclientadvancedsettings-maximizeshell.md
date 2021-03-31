---
title: Propriedade IMsRdpClientAdvancedSettings MaximizeShell
description: Especifica se os programas iniciados com a propriedade StartProgram devem ser maximizados.
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade MaximizeShell
- Propriedade MaximizeShell Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade MaximizeShell
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c172dd71fcf57f2028f6ba64c93ceaeec2ffb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918202"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a><span data-ttu-id="d6f65-120">Propriedade IMsRdpClientAdvancedSettings:: MaximizeShell</span><span class="sxs-lookup"><span data-stu-id="d6f65-120">IMsRdpClientAdvancedSettings::MaximizeShell property</span></span>

<span data-ttu-id="d6f65-121">Especifica se os programas iniciados com a propriedade [**StartProgram**](imstscsecuredsettings-startprogram.md) devem ser maximizados.</span><span class="sxs-lookup"><span data-stu-id="d6f65-121">Specifies if programs launched with the [**StartProgram**](imstscsecuredsettings-startprogram.md) property should be maximized.</span></span>

<span data-ttu-id="d6f65-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d6f65-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f65-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6f65-123">Syntax</span></span>


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
);
```



## <a name="property-value"></a><span data-ttu-id="d6f65-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d6f65-124">Property value</span></span>

<span data-ttu-id="d6f65-125">Defina esse parâmetro como 0 para desabilitar o recurso ou um valor diferente de zero para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="d6f65-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6f65-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d6f65-126">Error codes</span></span>

<span data-ttu-id="d6f65-127">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d6f65-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f65-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6f65-128">Remarks</span></span>

<span data-ttu-id="d6f65-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d6f65-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f65-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f65-130">Requirements</span></span>



| <span data-ttu-id="d6f65-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f65-131">Requirement</span></span> | <span data-ttu-id="d6f65-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d6f65-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f65-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f65-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f65-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6f65-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d6f65-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f65-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f65-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6f65-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d6f65-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d6f65-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6f65-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f65-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d6f65-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d6f65-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f65-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f65-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d6f65-141">IID</span><span class="sxs-lookup"><span data-stu-id="d6f65-141">IID</span></span><br/>                      | <span data-ttu-id="d6f65-142">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d6f65-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6f65-143">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6f65-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f65-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d6f65-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d6f65-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d6f65-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d6f65-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d6f65-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d6f65-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d6f65-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d6f65-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d6f65-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d6f65-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d6f65-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d6f65-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d6f65-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d6f65-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d6f65-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





