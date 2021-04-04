---
title: Código de notificação de NM_LDOWN (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que o botão esquerdo do mouse foi pressionado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- Código de notificação de NM_LDOWN (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824155"
---
# <a name="nm_ldown-toolbar-notification-code"></a><span data-ttu-id="eafa5-105">\_Código de notificação nm LDOWN (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="eafa5-105">NM\_LDOWN (toolbar) notification code</span></span>

<span data-ttu-id="eafa5-106">Notifica uma janela pai da barra de ferramentas que o botão esquerdo do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="eafa5-106">Notifies a toolbar's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="eafa5-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eafa5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="eafa5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eafa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafa5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eafa5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eafa5-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="eafa5-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="eafa5-111">Se o mouse tiver sido clicado em um item da barra de ferramentas, o membro **dwItemSpec** conterá o identificador de item e o membro **dwItemData** conterá os dados do item.</span><span class="sxs-lookup"><span data-stu-id="eafa5-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="eafa5-112">Se o mouse tiver sido clicado em um separador ou espaço em branco na barra de ferramentas, o membro **dwItemSpec** conterá-1.</span><span class="sxs-lookup"><span data-stu-id="eafa5-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eafa5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eafa5-113">Return value</span></span>

<span data-ttu-id="eafa5-114">Retorna **false** para permitir que o controle Toolbar execute o processamento padrão do evento ou **true** para impedir que o controle processe o evento.</span><span class="sxs-lookup"><span data-stu-id="eafa5-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="remarks"></a><span data-ttu-id="eafa5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="eafa5-115">Remarks</span></span>

<span data-ttu-id="eafa5-116">Essa notificação é enviada após o código de notificação do [tbn \_ DROPDOWN](tbn-dropdown.md) ser enviado.</span><span class="sxs-lookup"><span data-stu-id="eafa5-116">This notification is sent after the [TBN\_DROPDOWN](tbn-dropdown.md) notification code has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="eafa5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eafa5-117">Requirements</span></span>



| <span data-ttu-id="eafa5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eafa5-118">Requirement</span></span> | <span data-ttu-id="eafa5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="eafa5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eafa5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eafa5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eafa5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eafa5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eafa5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eafa5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eafa5-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eafa5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eafa5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eafa5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eafa5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eafa5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





