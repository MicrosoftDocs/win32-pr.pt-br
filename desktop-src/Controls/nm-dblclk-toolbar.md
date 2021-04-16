---
title: Código de notificação de NM_DBLCLK (barra de ferramentas) (commctrl. h)
description: Notifica a janela pai de um controle ToolBar que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- Código de notificação de NM_DBLCLK (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5441f86fa47f25a98dad82f9bfde05a84b5f498
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454625"
---
# <a name="nm_dblclk-toolbar-notification-code"></a><span data-ttu-id="41ef7-105">\_Código de notificação nm DBLCLK (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="41ef7-105">NM\_DBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="41ef7-106">Notifica a janela pai de um controle ToolBar que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="41ef7-106">Notifies the parent window of a toolbar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="41ef7-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="41ef7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="41ef7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41ef7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ef7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41ef7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41ef7-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="41ef7-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="41ef7-111">Se o mouse tiver sido clicado em um item da barra de ferramentas, o membro **dwItemSpec** conterá o identificador de item e o membro **dwItemData** conterá os dados do item.</span><span class="sxs-lookup"><span data-stu-id="41ef7-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="41ef7-112">Se o mouse tiver sido clicado em um separador ou espaço em branco na barra de ferramentas, o membro **dwItemSpec** conterá-1.</span><span class="sxs-lookup"><span data-stu-id="41ef7-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ef7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41ef7-113">Return value</span></span>

<span data-ttu-id="41ef7-114">Retorna **false** para permitir que o controle Toolbar execute o processamento padrão do evento ou **true** para impedir que o controle processe o evento.</span><span class="sxs-lookup"><span data-stu-id="41ef7-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ef7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ef7-115">Requirements</span></span>



| <span data-ttu-id="41ef7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ef7-116">Requirement</span></span> | <span data-ttu-id="41ef7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="41ef7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41ef7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ef7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="41ef7-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41ef7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41ef7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ef7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="41ef7-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41ef7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41ef7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41ef7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="41ef7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41ef7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





