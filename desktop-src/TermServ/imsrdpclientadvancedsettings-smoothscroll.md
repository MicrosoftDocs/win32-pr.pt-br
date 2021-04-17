---
title: Propriedade IMsRdpClientAdvancedSettings SmoothScroll
description: Não há suporte a esta propriedade. | Propriedade IMsRdpClientAdvancedSettings SmoothScroll
ms.assetid: 7f1ce439-0b6e-4426-8dd6-3748509130e1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade SmoothScroll
- Propriedade SmoothScroll Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade SmoothScroll
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmoothScroll
- IMsRdpClientAdvancedSettings.get_SmoothScroll
- IMsRdpClientAdvancedSettings.put_SmoothScroll
- IMsRdpClientAdvancedSettings2.SmoothScroll
- IMsRdpClientAdvancedSettings2.get_SmoothScroll
- IMsRdpClientAdvancedSettings2.put_SmoothScroll
- IMsRdpClientAdvancedSettings3.SmoothScroll
- IMsRdpClientAdvancedSettings3.get_SmoothScroll
- IMsRdpClientAdvancedSettings3.put_SmoothScroll
- IMsRdpClientAdvancedSettings4.SmoothScroll
- IMsRdpClientAdvancedSettings4.get_SmoothScroll
- IMsRdpClientAdvancedSettings4.put_SmoothScroll
- IMsRdpClientAdvancedSettings5.SmoothScroll
- IMsRdpClientAdvancedSettings5.get_SmoothScroll
- IMsRdpClientAdvancedSettings5.put_SmoothScroll
- IMsRdpClientAdvancedSettings6.SmoothScroll
- IMsRdpClientAdvancedSettings6.get_SmoothScroll
- IMsRdpClientAdvancedSettings6.put_SmoothScroll
- IMsRdpClientAdvancedSettings7.SmoothScroll
- IMsRdpClientAdvancedSettings7.get_SmoothScroll
- IMsRdpClientAdvancedSettings7.put_SmoothScroll
- IMsRdpClientAdvancedSettings8.SmoothScroll
- IMsRdpClientAdvancedSettings8.get_SmoothScroll
- IMsRdpClientAdvancedSettings8.put_SmoothScroll
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62be8fe85415792116c23b4e12d9ab56fb89e0f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105768552"
---
# <a name="imsrdpclientadvancedsettingssmoothscroll-property"></a><span data-ttu-id="27a20-121">Propriedade IMsRdpClientAdvancedSettings:: SmoothScroll</span><span class="sxs-lookup"><span data-stu-id="27a20-121">IMsRdpClientAdvancedSettings::SmoothScroll property</span></span>

<span data-ttu-id="27a20-122">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="27a20-122">This property is not supported.</span></span>

<span data-ttu-id="27a20-123">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="27a20-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a20-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="27a20-124">Syntax</span></span>


```C++
HRESULT put_SmoothScroll(
  [in]  LONG smoothScroll
);

HRESULT get_SmoothScroll(
  [out] LONG *psmoothScroll
);
```



## <a name="property-value"></a><span data-ttu-id="27a20-125">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="27a20-125">Property value</span></span>

<span data-ttu-id="27a20-126">Defina esse parâmetro como 0 para desabilitar a rolagem suave ou um valor diferente de zero para habilitar a rolagem suave.</span><span class="sxs-lookup"><span data-stu-id="27a20-126">Set this parameter to 0 to disable smooth scrolling or a nonzero value to enable smooth scrolling.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27a20-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="27a20-127">Error codes</span></span>

<span data-ttu-id="27a20-128">Retorna **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="27a20-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="27a20-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27a20-129">Requirements</span></span>



| <span data-ttu-id="27a20-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="27a20-130">Requirement</span></span> | <span data-ttu-id="27a20-131">Valor</span><span class="sxs-lookup"><span data-stu-id="27a20-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a20-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27a20-132">Minimum supported client</span></span><br/> | <span data-ttu-id="27a20-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="27a20-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="27a20-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27a20-134">Minimum supported server</span></span><br/> | <span data-ttu-id="27a20-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="27a20-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="27a20-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="27a20-136">End of client support</span></span><br/>    | <span data-ttu-id="27a20-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="27a20-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="27a20-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="27a20-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="27a20-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27a20-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="27a20-140">DLL</span><span class="sxs-lookup"><span data-stu-id="27a20-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27a20-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27a20-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="27a20-142">IID</span><span class="sxs-lookup"><span data-stu-id="27a20-142">IID</span></span><br/>                      | <span data-ttu-id="27a20-143">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="27a20-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27a20-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="27a20-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a20-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="27a20-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="27a20-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="27a20-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="27a20-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="27a20-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="27a20-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="27a20-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="27a20-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="27a20-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="27a20-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="27a20-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="27a20-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="27a20-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="27a20-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="27a20-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





