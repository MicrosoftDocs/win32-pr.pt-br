---
title: Propriedade IMsRdpClientNonScriptable4 WarnAboutPrinterRedirection
description: Controla se a caixa de diálogo redirecionamento exibe uma mensagem sobre o redirecionamento de impressora antes de iniciar uma sessão.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
- Propriedade WarnAboutPrinterRedirection Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295809"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="2cb0a-116">Propriedade IMsRdpClientNonScriptable4:: WarnAboutPrinterRedirection</span><span class="sxs-lookup"><span data-stu-id="2cb0a-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="2cb0a-117">Controla se a caixa de diálogo redirecionamento exibe uma mensagem sobre o redirecionamento de impressora antes de iniciar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="2cb0a-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb0a-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cb0a-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="2cb0a-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2cb0a-120">Property value</span></span>

<span data-ttu-id="2cb0a-121">Define se a caixa de diálogo de redirecionamento exibe uma mensagem sobre o redirecionamento de impressora.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2cb0a-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2cb0a-122">Error codes</span></span>

<span data-ttu-id="2cb0a-123">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb0a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb0a-124">Requirements</span></span>



| <span data-ttu-id="2cb0a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb0a-125">Requirement</span></span> | <span data-ttu-id="2cb0a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2cb0a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb0a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cb0a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb0a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cb0a-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2cb0a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cb0a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb0a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cb0a-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2cb0a-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2cb0a-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cb0a-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb0a-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2cb0a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb0a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb0a-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb0a-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2cb0a-135">IID</span><span class="sxs-lookup"><span data-stu-id="2cb0a-135">IID</span></span><br/>                      | <span data-ttu-id="2cb0a-136">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="2cb0a-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cb0a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cb0a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb0a-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2cb0a-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2cb0a-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2cb0a-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





