---
title: Propriedade IMsRdpClientNonScriptable4 MarkRdpSettingsSecure
description: Especifica se as configurações de protocolo RDP (RDP) são marcadas como seguras.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MarkRdpSettingsSecure
- Propriedade MarkRdpSettingsSecure Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade MarkRdpSettingsSecure
- Propriedade MarkRdpSettingsSecure Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade MarkRdpSettingsSecure
- Propriedade MarkRdpSettingsSecure Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade MarkRdpSettingsSecure
- Propriedade MarkRdpSettingsSecure Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade MarkRdpSettingsSecure
- Propriedade MarkRdpSettingsSecure Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade MarkRdpSettingsSecure
- Propriedade MarkRdpSettingsSecure Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade MarkRdpSettingsSecure
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499470"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="8eb26-116">Propriedade IMsRdpClientNonScriptable4:: MarkRdpSettingsSecure</span><span class="sxs-lookup"><span data-stu-id="8eb26-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="8eb26-117">Especifica se as configurações de [protocolo RDP](remote-desktop-protocol.md) (RDP) são marcadas como seguras.</span><span class="sxs-lookup"><span data-stu-id="8eb26-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="8eb26-118">Isso indica que as configurações aplicadas ao controle foram assinadas por um fornecedor confiável ou de terceiros.</span><span class="sxs-lookup"><span data-stu-id="8eb26-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="8eb26-119">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8eb26-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb26-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eb26-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="8eb26-121">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8eb26-121">Property value</span></span>

<span data-ttu-id="8eb26-122">Define se as configurações de RDP são marcadas como seguras.</span><span class="sxs-lookup"><span data-stu-id="8eb26-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8eb26-123">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8eb26-123">Error codes</span></span>

<span data-ttu-id="8eb26-124">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8eb26-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb26-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb26-125">Requirements</span></span>



| <span data-ttu-id="8eb26-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb26-126">Requirement</span></span> | <span data-ttu-id="8eb26-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb26-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb26-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb26-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb26-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eb26-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8eb26-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb26-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb26-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eb26-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8eb26-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8eb26-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="8eb26-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb26-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="8eb26-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb26-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb26-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb26-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="8eb26-136">IID</span><span class="sxs-lookup"><span data-stu-id="8eb26-136">IID</span></span><br/>                      | <span data-ttu-id="8eb26-137">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="8eb26-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8eb26-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eb26-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb26-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8eb26-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="8eb26-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="8eb26-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





