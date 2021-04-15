---
title: Propriedade IMsRdpClientNonScriptable2 UIParentWindowHandle
description: Define ou recupera o identificador de janela como a janela pai de qualquer caixa de diálogo exibida pelo controle. Isso permite que qualquer janela exibida pelo controle seja devidamente modal com relação a todas as janelas exibidas pelo aplicativo pai.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade UIParentWindowHandle
- Propriedade UIParentWindowHandle Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade UIParentWindowHandle
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454649"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="6d8f2-113">Propriedade IMsRdpClientNonScriptable2:: UIParentWindowHandle</span><span class="sxs-lookup"><span data-stu-id="6d8f2-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="6d8f2-114">Define ou recupera o identificador de janela como a janela pai de qualquer caixa de diálogo exibida pelo controle.</span><span class="sxs-lookup"><span data-stu-id="6d8f2-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="6d8f2-115">Isso permite que qualquer janela exibida pelo controle seja devidamente modal com relação a todas as janelas exibidas pelo aplicativo pai.</span><span class="sxs-lookup"><span data-stu-id="6d8f2-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="6d8f2-116">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6d8f2-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d8f2-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d8f2-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="6d8f2-118">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d8f2-118">Property value</span></span>

<span data-ttu-id="6d8f2-119">O novo identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="6d8f2-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d8f2-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6d8f2-120">Error codes</span></span>

<span data-ttu-id="6d8f2-121">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6d8f2-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8f2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d8f2-122">Remarks</span></span>

<span data-ttu-id="6d8f2-123">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6d8f2-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8f2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8f2-124">Requirements</span></span>



| <span data-ttu-id="6d8f2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8f2-125">Requirement</span></span> | <span data-ttu-id="6d8f2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6d8f2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8f2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8f2-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d8f2-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="6d8f2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8f2-130">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="6d8f2-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="6d8f2-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6d8f2-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d8f2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d8f2-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6d8f2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6d8f2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d8f2-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d8f2-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6d8f2-135">IID</span><span class="sxs-lookup"><span data-stu-id="6d8f2-135">IID</span></span><br/>                      | <span data-ttu-id="6d8f2-136">IID \_ IMsRdpClientNonScriptable2 é definido como 17a5e535-4072-4fa4-AF32-c8d0d47345e9</span><span class="sxs-lookup"><span data-stu-id="6d8f2-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d8f2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d8f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8f2-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6d8f2-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="6d8f2-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6d8f2-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="6d8f2-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6d8f2-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6d8f2-141">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="6d8f2-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="6d8f2-142">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="6d8f2-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="6d8f2-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="6d8f2-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





