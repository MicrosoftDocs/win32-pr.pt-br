---
title: Código de notificação de NM_RDBLCLK (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai do controle que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- Código de notificação de NM_RDBLCLK (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455659"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a><span data-ttu-id="7379c-105">\_Código de notificação nm RDBLCLK (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="7379c-105">NM\_RDBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="7379c-106">Notifica uma janela pai do controle que o usuário clicou duas vezes com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="7379c-106">Notifies a control's parent window that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="7379c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7379c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7379c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7379c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7379c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7379c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7379c-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="7379c-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="7379c-111">Se o mouse tiver sido clicado em um item da barra de ferramentas, o membro **dwItemSpec** conterá o identificador de item e o membro **dwItemData** conterá os dados do item.</span><span class="sxs-lookup"><span data-stu-id="7379c-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="7379c-112">Se o mouse tiver sido clicado em um separador ou espaço em branco na barra de ferramentas, o membro **dwItemSpec** conterá-1.</span><span class="sxs-lookup"><span data-stu-id="7379c-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7379c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7379c-113">Return value</span></span>

<span data-ttu-id="7379c-114">Retorna **false** para permitir que o controle Toolbar execute o processamento padrão do evento ou **true** para impedir que o controle processe o evento.</span><span class="sxs-lookup"><span data-stu-id="7379c-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7379c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7379c-115">Requirements</span></span>



| <span data-ttu-id="7379c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7379c-116">Requirement</span></span> | <span data-ttu-id="7379c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7379c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7379c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7379c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7379c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7379c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7379c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7379c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7379c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7379c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7379c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7379c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7379c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7379c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





