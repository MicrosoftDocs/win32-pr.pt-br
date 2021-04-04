---
title: Propriedade IMsRdpClientAdvancedSettings5 RedirectClipboard
description: Define ou recupera a configuração para o redirecionamento da área de transferência.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectClipboard
- Propriedade RedirectClipboard Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectClipboard
- Propriedade RedirectClipboard Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectClipboard
- Propriedade RedirectClipboard Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectClipboard
- Propriedade RedirectClipboard Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectClipboard
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918200"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="71530-112">Propriedade IMsRdpClientAdvancedSettings5:: RedirectClipboard</span><span class="sxs-lookup"><span data-stu-id="71530-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="71530-113">Define ou recupera a configuração para o redirecionamento da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="71530-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="71530-114">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="71530-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71530-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="71530-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="71530-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="71530-116">Property value</span></span>

<span data-ttu-id="71530-117">Define o modo de redirecionamento da área de transferência como **verdadeiro** ou **falso**.</span><span class="sxs-lookup"><span data-stu-id="71530-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="71530-118">Se definido como **true**, o modo de redirecionamento da área de transferência será habilitado.</span><span class="sxs-lookup"><span data-stu-id="71530-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="71530-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71530-119">Requirements</span></span>



| <span data-ttu-id="71530-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="71530-120">Requirement</span></span> | <span data-ttu-id="71530-121">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71530-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71530-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71530-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71530-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="71530-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71530-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71530-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71530-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="71530-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="71530-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="71530-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71530-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="71530-128">DLL</span><span class="sxs-lookup"><span data-stu-id="71530-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71530-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71530-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="71530-130">IID</span><span class="sxs-lookup"><span data-stu-id="71530-130">IID</span></span><br/>                      | <span data-ttu-id="71530-131">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="71530-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71530-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="71530-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71530-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="71530-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="71530-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="71530-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="71530-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="71530-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="71530-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="71530-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





