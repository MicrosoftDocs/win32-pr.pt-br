---
title: TBN_DROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica em um botão suspenso. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918264"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="d4235-105">\_Código de notificação da lista suspensa tbn</span><span class="sxs-lookup"><span data-stu-id="d4235-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="d4235-106">Enviado por um controle Toolbar quando o usuário clica em um botão suspenso.</span><span class="sxs-lookup"><span data-stu-id="d4235-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="d4235-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d4235-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d4235-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4235-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4235-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4235-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4235-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="d4235-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="d4235-111">Para este código de notificação, somente os membros **HDR** e **iItem** dessa estrutura são válidos.</span><span class="sxs-lookup"><span data-stu-id="d4235-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4235-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4235-112">Return value</span></span>

<span data-ttu-id="d4235-113">Retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d4235-113">Returns one of the following values:</span></span>



| <span data-ttu-id="d4235-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d4235-114">Return code</span></span>                                                                                          | <span data-ttu-id="d4235-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4235-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4235-116"><dt>**TBDDRET \_ padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="d4235-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="d4235-117">A lista suspensa foi tratada.</span><span class="sxs-lookup"><span data-stu-id="d4235-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="d4235-118"><dt>**TBDDRET \_ padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="d4235-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="d4235-119">A lista suspensa não foi tratada.</span><span class="sxs-lookup"><span data-stu-id="d4235-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="d4235-120"><dt>**TBDDRET \_ TREATPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="d4235-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="d4235-121">A lista suspensa foi tratada, mas trata o botão como um botão normal.</span><span class="sxs-lookup"><span data-stu-id="d4235-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4235-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4235-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4235-123">Os botões suspensos podem ser simples (estilo de [**\_ lista suspensa BTNS**](toolbar-control-and-button-styles.md) ), exibir uma seta ao lado da imagem do botão (estilo [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) ) ou exibir uma seta que é separada do estilo da imagem ([**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="d4235-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="d4235-124">Se uma seta separada for usada, \_ a lista suspensa tbn será enviada somente se o usuário clicar na parte de seta do botão.</span><span class="sxs-lookup"><span data-stu-id="d4235-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="d4235-125">Se o usuário clicar na parte principal do botão, uma mensagem [**de \_ comando do WM**](/windows/desktop/menurc/wm-command) com a ID do botão será enviada, assim como com um botão padrão.</span><span class="sxs-lookup"><span data-stu-id="d4235-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="d4235-126">Para os outros dois estilos de botão suspenso, a \_ lista suspensa tbn é enviada quando o usuário clica em qualquer parte do botão.</span><span class="sxs-lookup"><span data-stu-id="d4235-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4235-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4235-127">Requirements</span></span>



| <span data-ttu-id="d4235-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4235-128">Requirement</span></span> | <span data-ttu-id="d4235-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d4235-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4235-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4235-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d4235-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4235-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4235-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4235-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d4235-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4235-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4235-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4235-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4235-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4235-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

