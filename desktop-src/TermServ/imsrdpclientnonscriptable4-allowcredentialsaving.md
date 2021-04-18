---
title: Propriedade IMsRdpClientNonScriptable4 AllowCredentialSaving
description: Especifica se a caixa de diálogo credenciais exibe uma caixa de seleção que habilita o salvamento de credenciais.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade AllowCredentialSaving
- Propriedade AllowCredentialSaving Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800004"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="b4179-116">Propriedade IMsRdpClientNonScriptable4:: AllowCredentialSaving</span><span class="sxs-lookup"><span data-stu-id="b4179-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="b4179-117">Especifica se a caixa de diálogo credenciais exibe uma caixa de seleção que habilita o salvamento de credenciais.</span><span class="sxs-lookup"><span data-stu-id="b4179-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="b4179-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b4179-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4179-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4179-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="b4179-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b4179-120">Property value</span></span>

<span data-ttu-id="b4179-121">Define se a caixa de diálogo credenciais exibe uma caixa de seleção que habilita o salvamento de credenciais.</span><span class="sxs-lookup"><span data-stu-id="b4179-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4179-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b4179-122">Error codes</span></span>

<span data-ttu-id="b4179-123">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b4179-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4179-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4179-124">Requirements</span></span>



| <span data-ttu-id="b4179-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4179-125">Requirement</span></span> | <span data-ttu-id="b4179-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b4179-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4179-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4179-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b4179-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4179-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b4179-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4179-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b4179-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4179-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b4179-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b4179-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4179-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4179-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b4179-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b4179-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4179-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4179-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b4179-135">IID</span><span class="sxs-lookup"><span data-stu-id="b4179-135">IID</span></span><br/>                      | <span data-ttu-id="b4179-136">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="b4179-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4179-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4179-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4179-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b4179-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="b4179-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="b4179-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





