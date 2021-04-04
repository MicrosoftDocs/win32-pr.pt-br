---
title: Código de notificação de NM_CLICK (barra de ferramentas) (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Código de notificação de NM_CLICK (barra de ferramentas) controles do Windows
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
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824853"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="55f41-105">\_Código de notificação de clique do nm (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="55f41-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="55f41-106">Enviado por um controle Toolbar quando o usuário clica em um item com o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="55f41-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="55f41-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="55f41-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="55f41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55f41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55f41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55f41-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="55f41-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="55f41-111">O membro **dwItemSpec** contém o índice da seção que foi clicada.</span><span class="sxs-lookup"><span data-stu-id="55f41-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f41-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55f41-112">Return value</span></span>

<span data-ttu-id="55f41-113">Retornar **true** para indicar que o clique do mouse foi tratado e suprimir o processamento padrão pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="55f41-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="55f41-114">Retorne **false** para permitir o processamento padrão do clique.</span><span class="sxs-lookup"><span data-stu-id="55f41-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="55f41-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="55f41-115">Remarks</span></span>

<span data-ttu-id="55f41-116">Clicar em um item com o botão esquerdo do mouse faz com que a barra de ferramentas envie uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) com o código de notificação [ \_ clicado bilhão](bn-clicked.md) para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="55f41-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="55f41-117">A notificação de clique de NM \_ é enviada após a mensagem de **\_ comando do WM** .</span><span class="sxs-lookup"><span data-stu-id="55f41-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f41-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55f41-118">Requirements</span></span>



| <span data-ttu-id="55f41-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f41-119">Requirement</span></span> | <span data-ttu-id="55f41-120">Valor</span><span class="sxs-lookup"><span data-stu-id="55f41-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55f41-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55f41-121">Minimum supported client</span></span><br/> | <span data-ttu-id="55f41-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55f41-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55f41-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55f41-123">Minimum supported server</span></span><br/> | <span data-ttu-id="55f41-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55f41-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55f41-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55f41-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="55f41-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f41-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

