---
title: Propriedade IMsTscNonScriptable BinarySalt
description: Esta propriedade não está mais disponível para uso. | Propriedade IMsTscNonScriptable BinarySalt
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, Propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, objeto MsTscAx
- Objeto MsTscAx Serviços de Área de Trabalho Remota, Propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, Propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade BinarySalt
- Propriedade BinarySalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade BinarySalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb13ccb79a9cf2c309a32772a73b393756c7bdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105757595"
---
# <a name="imstscnonscriptablebinarysalt-property"></a><span data-ttu-id="54afa-119">Propriedade IMsTscNonScriptable:: BinarySalt</span><span class="sxs-lookup"><span data-stu-id="54afa-119">IMsTscNonScriptable::BinarySalt property</span></span>

<span data-ttu-id="54afa-120">Esta propriedade não está mais disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="54afa-120">This property is no longer available for use.</span></span>

<span data-ttu-id="54afa-121">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="54afa-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54afa-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="54afa-122">Syntax</span></span>


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a><span data-ttu-id="54afa-123">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="54afa-123">Property value</span></span>

<span data-ttu-id="54afa-124">A nova parte de Salt binário de uma senha codificada binária.</span><span class="sxs-lookup"><span data-stu-id="54afa-124">The new binary salt part for a binary encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="54afa-125">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="54afa-125">Error codes</span></span>

<span data-ttu-id="54afa-126">Retorna **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="54afa-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54afa-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54afa-127">Requirements</span></span>



| <span data-ttu-id="54afa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="54afa-128">Requirement</span></span> | <span data-ttu-id="54afa-129">Valor</span><span class="sxs-lookup"><span data-stu-id="54afa-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54afa-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54afa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54afa-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54afa-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54afa-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54afa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54afa-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54afa-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54afa-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="54afa-134">End of client support</span></span><br/>    | <span data-ttu-id="54afa-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54afa-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54afa-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="54afa-136">End of server support</span></span><br/>    | <span data-ttu-id="54afa-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54afa-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54afa-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="54afa-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="54afa-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54afa-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="54afa-140">DLL</span><span class="sxs-lookup"><span data-stu-id="54afa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54afa-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54afa-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="54afa-142">IID</span><span class="sxs-lookup"><span data-stu-id="54afa-142">IID</span></span><br/>                      | <span data-ttu-id="54afa-143">IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="54afa-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54afa-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="54afa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54afa-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="54afa-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="54afa-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="54afa-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="54afa-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="54afa-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="54afa-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="54afa-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="54afa-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="54afa-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="54afa-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="54afa-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





