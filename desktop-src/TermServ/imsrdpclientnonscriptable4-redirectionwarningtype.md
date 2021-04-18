---
title: Propriedade IMsRdpClientNonScriptable4 RedirectionWarningType
description: Controla a presença e a aparência da caixa de diálogo que notifica o usuário sobre o redirecionamento.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectionWarningType
- Propriedade RedirectionWarningType Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade RedirectionWarningType
- Propriedade RedirectionWarningType Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade RedirectionWarningType
- Propriedade RedirectionWarningType Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade RedirectionWarningType
- Propriedade RedirectionWarningType Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade RedirectionWarningType
- Propriedade RedirectionWarningType Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade RedirectionWarningType
- Propriedade RedirectionWarningType Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade RedirectionWarningType
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767725"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="0b733-116">Propriedade IMsRdpClientNonScriptable4:: RedirectionWarningType</span><span class="sxs-lookup"><span data-stu-id="0b733-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="0b733-117">Controla a presença e a aparência da caixa de diálogo que notifica o usuário sobre o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="0b733-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="0b733-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0b733-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b733-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b733-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="0b733-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0b733-120">Property value</span></span>

<span data-ttu-id="0b733-121">Define o tipo da caixa de diálogo que notifica o usuário sobre o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="0b733-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="0b733-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="0b733-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-123">A caixa de diálogo não é específica do editor.</span><span class="sxs-lookup"><span data-stu-id="0b733-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="0b733-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="0b733-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-125">A caixa de diálogo é para arquivos não assinados.</span><span class="sxs-lookup"><span data-stu-id="0b733-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="0b733-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="0b733-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-127">A caixa de diálogo é para um Publicador desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0b733-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="0b733-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span><span class="sxs-lookup"><span data-stu-id="0b733-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-129">A caixa de diálogo é para os arquivos do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b733-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="0b733-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="0b733-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-131">A caixa de diálogo é exibida para arquivos assinados com certificação de terceiros.</span><span class="sxs-lookup"><span data-stu-id="0b733-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="0b733-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="0b733-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-133">A caixa de diálogo não é exibida porque o aplicativo é publicado por um fornecedor confiável.</span><span class="sxs-lookup"><span data-stu-id="0b733-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="0b733-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="0b733-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="0b733-135">A caixa de diálogo não é exibida porque o aplicativo é publicado por um fornecedor confiável.</span><span class="sxs-lookup"><span data-stu-id="0b733-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="0b733-136">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0b733-136">Error codes</span></span>

<span data-ttu-id="0b733-137">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0b733-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b733-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b733-138">Remarks</span></span>

<span data-ttu-id="0b733-139">O valor **RedirectionWarningTypeDefault**, que é o valor padrão dessa propriedade, exerce nenhum controle sobre a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0b733-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="0b733-140">Nesse caso, a propriedade de controle é [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) em [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span><span class="sxs-lookup"><span data-stu-id="0b733-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b733-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b733-141">Requirements</span></span>



| <span data-ttu-id="0b733-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b733-142">Requirement</span></span> | <span data-ttu-id="0b733-143">Valor</span><span class="sxs-lookup"><span data-stu-id="0b733-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b733-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b733-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0b733-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b733-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0b733-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b733-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0b733-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b733-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b733-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0b733-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b733-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b733-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0b733-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0b733-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b733-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b733-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0b733-152">IID</span><span class="sxs-lookup"><span data-stu-id="0b733-152">IID</span></span><br/>                      | <span data-ttu-id="0b733-153">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="0b733-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b733-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b733-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b733-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="0b733-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="0b733-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0b733-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





