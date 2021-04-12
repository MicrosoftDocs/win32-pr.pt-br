---
title: Propriedade IMsRdpClientNonScriptable3 PromptForCredentials (WUAPI. h)
description: Especifica ou recupera se a caixa de diálogo solicitar credenciais está habilitada para a conexão.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade PromptForCredentials
- Propriedade PromptForCredentials Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade PromptForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294758"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="a7f9d-120">IMsRdpClientNonScriptable3: Propriedade romptForCredentials de:P</span><span class="sxs-lookup"><span data-stu-id="a7f9d-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="a7f9d-121">Especifica ou recupera se a caixa de diálogo solicitar credenciais está habilitada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="a7f9d-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f9d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f9d-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="a7f9d-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a7f9d-124">Property value</span></span>

<span data-ttu-id="a7f9d-125">Especifica se a caixa de diálogo solicitar credenciais está habilitada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7f9d-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a7f9d-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f9d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7f9d-127">Requirements</span></span>



| <span data-ttu-id="a7f9d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f9d-128">Requirement</span></span> | <span data-ttu-id="a7f9d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a7f9d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f9d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7f9d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f9d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7f9d-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a7f9d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7f9d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f9d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7f9d-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a7f9d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7f9d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f9d-135"><dt>WUAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f9d-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="a7f9d-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a7f9d-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7f9d-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7f9d-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a7f9d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a7f9d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7f9d-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7f9d-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a7f9d-140">IID</span><span class="sxs-lookup"><span data-stu-id="a7f9d-140">IID</span></span><br/>                      | <span data-ttu-id="a7f9d-141">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="a7f9d-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7f9d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7f9d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f9d-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a7f9d-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a7f9d-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a7f9d-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a7f9d-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="a7f9d-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





