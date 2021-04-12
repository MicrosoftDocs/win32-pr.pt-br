---
title: Propriedade IMsRdpClientNonScriptable4 PromptForCredsOnClient
description: Especifica se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
- Propriedade PromptForCredsOnClient Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369734"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="a187d-116">IMsRdpClientNonScriptable4: Propriedade romptForCredsOnClient de:P</span><span class="sxs-lookup"><span data-stu-id="a187d-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="a187d-117">Especifica se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.</span><span class="sxs-lookup"><span data-stu-id="a187d-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="a187d-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a187d-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a187d-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="a187d-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="a187d-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a187d-120">Property value</span></span>

<span data-ttu-id="a187d-121">Define se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.</span><span class="sxs-lookup"><span data-stu-id="a187d-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a187d-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a187d-122">Error codes</span></span>

<span data-ttu-id="a187d-123">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a187d-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a187d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a187d-124">Requirements</span></span>



| <span data-ttu-id="a187d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a187d-125">Requirement</span></span> | <span data-ttu-id="a187d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a187d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a187d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a187d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a187d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a187d-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a187d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a187d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a187d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a187d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a187d-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a187d-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="a187d-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a187d-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a187d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a187d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a187d-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a187d-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a187d-135">IID</span><span class="sxs-lookup"><span data-stu-id="a187d-135">IID</span></span><br/>                      | <span data-ttu-id="a187d-136">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="a187d-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a187d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a187d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a187d-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a187d-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a187d-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a187d-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





