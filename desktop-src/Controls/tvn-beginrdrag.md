---
title: TVN_BEGINRDRAG código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore sobre a inicialização de uma operação de arrastar e soltar que envolve o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919073"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="e1e94-105">Código de notificação do TVN \_ BEGINRDRAG</span><span class="sxs-lookup"><span data-stu-id="e1e94-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="e1e94-106">Notifica uma janela pai do controle de exibição de árvore sobre a inicialização de uma operação de arrastar e soltar que envolve o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="e1e94-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="e1e94-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e1e94-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="e1e94-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1e94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1e94-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1e94-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1e94-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="e1e94-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="e1e94-111">O membro **itemNew** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas nos membros **hItem**, **estado** e **lParam** sobre o item a ser arrastado.</span><span class="sxs-lookup"><span data-stu-id="e1e94-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="e1e94-112">O membro **ptDrag** especifica as coordenadas de tela atuais do mouse.</span><span class="sxs-lookup"><span data-stu-id="e1e94-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1e94-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1e94-113">Return value</span></span>

<span data-ttu-id="e1e94-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e1e94-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e94-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1e94-115">Requirements</span></span>



| <span data-ttu-id="e1e94-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1e94-116">Requirement</span></span> | <span data-ttu-id="e1e94-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e1e94-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e94-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1e94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e94-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1e94-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1e94-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1e94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e94-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1e94-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1e94-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1e94-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1e94-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1e94-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e1e94-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e1e94-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1e94-125">**TVN \_ BEGINRDRAGW** (Unicode) e **TVN \_ BEGINRDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e1e94-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 





