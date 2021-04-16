---
title: Propriedade IMsTscAdvancedSettings BitmapPeristence
description: Especifica se o cache de bitmaps está habilitado.
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade BitmapPeristence
- Propriedade BitmapPeristence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BitmapPeristence
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455918"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a><span data-ttu-id="bada4-122">Propriedade IMsTscAdvancedSettings:: BitmapPeristence</span><span class="sxs-lookup"><span data-stu-id="bada4-122">IMsTscAdvancedSettings::BitmapPeristence property</span></span>

<span data-ttu-id="bada4-123">Especifica se o cache de bitmaps está habilitado.</span><span class="sxs-lookup"><span data-stu-id="bada4-123">Specifies whether bitmap caching is enabled.</span></span> <span data-ttu-id="bada4-124">O cache persistente pode melhorar o desempenho, mas requer espaço em disco adicional.</span><span class="sxs-lookup"><span data-stu-id="bada4-124">Persistent caching can improve performance but requires additional disk space.</span></span>

> [!Note]  
> <span data-ttu-id="bada4-125">O erro ortográfico no nome da propriedade e seu parâmetro está na versão de lançamento do controle.</span><span class="sxs-lookup"><span data-stu-id="bada4-125">The spelling error in the name of the property and its parameter is in the released version of the control.</span></span>

 

<span data-ttu-id="bada4-126">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bada4-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bada4-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="bada4-127">Syntax</span></span>


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="bada4-128">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bada4-128">Property value</span></span>

<span data-ttu-id="bada4-129">Defina esse parâmetro como 0 para desabilitar o cache ou um valor diferente de zero para habilitar o Caching.</span><span class="sxs-lookup"><span data-stu-id="bada4-129">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bada4-130">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bada4-130">Error codes</span></span>

<span data-ttu-id="bada4-131">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bada4-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bada4-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="bada4-132">Remarks</span></span>

<span data-ttu-id="bada4-133">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bada4-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bada4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bada4-134">Requirements</span></span>



| <span data-ttu-id="bada4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bada4-135">Requirement</span></span> | <span data-ttu-id="bada4-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bada4-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bada4-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bada4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bada4-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bada4-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="bada4-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bada4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bada4-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bada4-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bada4-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bada4-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="bada4-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bada4-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="bada4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bada4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bada4-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bada4-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="bada4-145">IID</span><span class="sxs-lookup"><span data-stu-id="bada4-145">IID</span></span><br/>                      | <span data-ttu-id="bada4-146">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="bada4-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bada4-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="bada4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bada4-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bada4-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bada4-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bada4-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bada4-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bada4-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="bada4-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bada4-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bada4-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bada4-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bada4-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bada4-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bada4-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bada4-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bada4-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bada4-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bada4-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bada4-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





