---
title: Propriedade IMsTscNonScriptable PortableSalt
description: Esta propriedade não é mais suportada.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, objeto MsTscAx
- Objeto MsTscAx Serviços de Área de Trabalho Remota, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PortableSalt
- Propriedade PortableSalt Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PortableSalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644871"
---
# <a name="imstscnonscriptableportablesalt-property"></a><span data-ttu-id="92cc5-118">IMsTscNonScriptable: Propriedade ortableSalt de:P</span><span class="sxs-lookup"><span data-stu-id="92cc5-118">IMsTscNonScriptable::PortableSalt property</span></span>

<span data-ttu-id="92cc5-119">Esta propriedade não é mais suportada.</span><span class="sxs-lookup"><span data-stu-id="92cc5-119">This property is no longer supported.</span></span>

<span data-ttu-id="92cc5-120">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="92cc5-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="92cc5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="92cc5-121">Syntax</span></span>


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a><span data-ttu-id="92cc5-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="92cc5-122">Property value</span></span>

<span data-ttu-id="92cc5-123">A nova parte de Salt portátil para uma senha codificada portátil.</span><span class="sxs-lookup"><span data-stu-id="92cc5-123">The new portable salt part for a portable encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92cc5-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="92cc5-124">Error codes</span></span>

<span data-ttu-id="92cc5-125">Retorna **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="92cc5-125">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92cc5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92cc5-126">Requirements</span></span>



| <span data-ttu-id="92cc5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="92cc5-127">Requirement</span></span> | <span data-ttu-id="92cc5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="92cc5-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92cc5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92cc5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="92cc5-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92cc5-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="92cc5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92cc5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="92cc5-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92cc5-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="92cc5-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="92cc5-133">End of client support</span></span><br/>    | <span data-ttu-id="92cc5-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92cc5-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="92cc5-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="92cc5-135">End of server support</span></span><br/>    | <span data-ttu-id="92cc5-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92cc5-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="92cc5-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="92cc5-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="92cc5-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92cc5-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="92cc5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="92cc5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92cc5-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92cc5-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="92cc5-141">IID</span><span class="sxs-lookup"><span data-stu-id="92cc5-141">IID</span></span><br/>                      | <span data-ttu-id="92cc5-142">IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="92cc5-142">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92cc5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="92cc5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92cc5-144">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="92cc5-144">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="92cc5-145">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="92cc5-145">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="92cc5-146">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="92cc5-146">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="92cc5-147">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="92cc5-147">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="92cc5-148">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="92cc5-148">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="92cc5-149">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="92cc5-149">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="92cc5-150">**PortablePassword**</span><span class="sxs-lookup"><span data-stu-id="92cc5-150">**PortablePassword**</span></span>](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





