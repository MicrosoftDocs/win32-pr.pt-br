---
title: Propriedade IMsTscNonScriptable BinaryPassword
description: Esta propriedade não está mais disponível para uso. | Propriedade IMsTscNonScriptable BinaryPassword
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, Propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, objeto MsTscAx
- Objeto MsTscAx Serviços de Área de Trabalho Remota, Propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, Propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade BinaryPassword
- Propriedade BinaryPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade BinaryPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105810434"
---
# <a name="imstscnonscriptablebinarypassword-property"></a><span data-ttu-id="5727b-119">Propriedade IMsTscNonScriptable:: BinaryPassword</span><span class="sxs-lookup"><span data-stu-id="5727b-119">IMsTscNonScriptable::BinaryPassword property</span></span>

<span data-ttu-id="5727b-120">Esta propriedade não está mais disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="5727b-120">This property is no longer available for use.</span></span>

<span data-ttu-id="5727b-121">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5727b-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5727b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5727b-122">Syntax</span></span>


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a><span data-ttu-id="5727b-123">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5727b-123">Property value</span></span>

<span data-ttu-id="5727b-124">A nova parte da senha, em formato binário codificado.</span><span class="sxs-lookup"><span data-stu-id="5727b-124">The new password part, in binary encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5727b-125">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5727b-125">Error codes</span></span>

<span data-ttu-id="5727b-126">Retorna **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="5727b-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5727b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5727b-127">Requirements</span></span>



| <span data-ttu-id="5727b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5727b-128">Requirement</span></span> | <span data-ttu-id="5727b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5727b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5727b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5727b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5727b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5727b-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5727b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5727b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5727b-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5727b-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5727b-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5727b-134">End of client support</span></span><br/>    | <span data-ttu-id="5727b-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5727b-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5727b-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5727b-136">End of server support</span></span><br/>    | <span data-ttu-id="5727b-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5727b-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5727b-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5727b-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="5727b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5727b-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5727b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5727b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5727b-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5727b-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5727b-142">IID</span><span class="sxs-lookup"><span data-stu-id="5727b-142">IID</span></span><br/>                      | <span data-ttu-id="5727b-143">IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="5727b-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5727b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5727b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5727b-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="5727b-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="5727b-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="5727b-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="5727b-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5727b-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="5727b-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5727b-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="5727b-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5727b-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5727b-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="5727b-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





