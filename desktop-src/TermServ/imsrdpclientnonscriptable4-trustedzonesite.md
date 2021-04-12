---
title: Propriedade IMsRdpClientNonScriptable4 TrustedZoneSite
description: Especifica se o site do qual o usuário iniciou a conexão está na lista de sites confiáveis do computador cliente do usuário.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TrustedZoneSite
- Propriedade TrustedZoneSite Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade TrustedZoneSite
- Propriedade TrustedZoneSite Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade TrustedZoneSite
- Propriedade TrustedZoneSite Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade TrustedZoneSite
- Propriedade TrustedZoneSite Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade TrustedZoneSite
- Propriedade TrustedZoneSite Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade TrustedZoneSite
- Propriedade TrustedZoneSite Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade TrustedZoneSite
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369733"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="bc529-116">Propriedade IMsRdpClientNonScriptable4:: TrustedZoneSite</span><span class="sxs-lookup"><span data-stu-id="bc529-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="bc529-117">Especifica se o site do qual o usuário iniciou a conexão está na lista de sites confiáveis do computador cliente do usuário.</span><span class="sxs-lookup"><span data-stu-id="bc529-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="bc529-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bc529-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc529-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc529-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="bc529-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bc529-120">Property value</span></span>

<span data-ttu-id="bc529-121">Define a propriedade TrustedZoneSite.</span><span class="sxs-lookup"><span data-stu-id="bc529-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="bc529-122">Esse método não tem efeito se o site do qual o usuário iniciou a conexão estiver na lista de sites confiáveis do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="bc529-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc529-123">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bc529-123">Error codes</span></span>

<span data-ttu-id="bc529-124">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bc529-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc529-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc529-125">Requirements</span></span>



| <span data-ttu-id="bc529-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc529-126">Requirement</span></span> | <span data-ttu-id="bc529-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bc529-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc529-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc529-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc529-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc529-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bc529-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc529-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc529-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc529-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bc529-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bc529-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc529-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc529-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bc529-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bc529-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc529-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc529-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bc529-136">IID</span><span class="sxs-lookup"><span data-stu-id="bc529-136">IID</span></span><br/>                      | <span data-ttu-id="bc529-137">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="bc529-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc529-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc529-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc529-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="bc529-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="bc529-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="bc529-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





