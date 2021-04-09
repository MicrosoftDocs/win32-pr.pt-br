---
title: Código de notificação NM_CLICK (Syslink) (commctrl. h)
description: Notifica uma janela pai do controle que o usuário clicou em um hiperlink com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Syslink (código de notificação de NM_CLICK) controles do Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086543"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="745c5-105">\_Código de notificação de clique do nm (Syslink)</span><span class="sxs-lookup"><span data-stu-id="745c5-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="745c5-106">Notifica uma janela pai do controle que o usuário clicou em um hiperlink com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="745c5-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="745c5-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="745c5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="745c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="745c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="745c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="745c5-110">Ponteiro para uma estrutura [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="745c5-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745c5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="745c5-111">Return value</span></span>

<span data-ttu-id="745c5-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="745c5-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="745c5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="745c5-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="745c5-114">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="745c5-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="745c5-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="745c5-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="745c5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="745c5-116">Requirements</span></span>



| <span data-ttu-id="745c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="745c5-117">Requirement</span></span> | <span data-ttu-id="745c5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="745c5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="745c5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="745c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="745c5-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="745c5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="745c5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="745c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="745c5-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="745c5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="745c5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="745c5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="745c5-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="745c5-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745c5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="745c5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="745c5-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="745c5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="745c5-127">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="745c5-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="745c5-128">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="745c5-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





