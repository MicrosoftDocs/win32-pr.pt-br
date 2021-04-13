---
title: Propriedade IMsRdpClient4 AdvancedSettings5
description: Recupera um ponteiro para uma interface IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings5
- Propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499788"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="80dd7-118">Propriedade IMsRdpClient4:: AdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="80dd7-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="80dd7-119">Recupera um ponteiro para uma interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="80dd7-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="80dd7-120">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="80dd7-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80dd7-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80dd7-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="80dd7-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="80dd7-122">Property value</span></span>

<span data-ttu-id="80dd7-123">Um ponteiro para a interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="80dd7-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="80dd7-124">A interface pode ser usada para definir configurações avançadas para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="80dd7-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80dd7-125">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="80dd7-125">Error codes</span></span>

<span data-ttu-id="80dd7-126">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="80dd7-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="80dd7-127">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="80dd7-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="80dd7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="80dd7-128">Remarks</span></span>

<span data-ttu-id="80dd7-129">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="80dd7-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="80dd7-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="80dd7-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80dd7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80dd7-131">Requirements</span></span>



| <span data-ttu-id="80dd7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="80dd7-132">Requirement</span></span> | <span data-ttu-id="80dd7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="80dd7-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80dd7-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80dd7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="80dd7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80dd7-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="80dd7-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80dd7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="80dd7-137">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="80dd7-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="80dd7-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="80dd7-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="80dd7-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80dd7-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="80dd7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="80dd7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80dd7-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80dd7-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="80dd7-142">IID</span><span class="sxs-lookup"><span data-stu-id="80dd7-142">IID</span></span><br/>                      | <span data-ttu-id="80dd7-143">IMsRdpClient4 é definido como 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span><span class="sxs-lookup"><span data-stu-id="80dd7-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="80dd7-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="80dd7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80dd7-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="80dd7-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="80dd7-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="80dd7-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="80dd7-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="80dd7-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="80dd7-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="80dd7-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="80dd7-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="80dd7-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="80dd7-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="80dd7-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="80dd7-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="80dd7-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





