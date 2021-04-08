---
title: TVN_SELCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a seleção está prestes a ser alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009256"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="2c842-105">Código de notificação do TVN \_ SELCHANGING</span><span class="sxs-lookup"><span data-stu-id="2c842-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="2c842-106">Notifica uma janela pai do controle de exibição de árvore que a seleção está prestes a ser alterada de um item para outro.</span><span class="sxs-lookup"><span data-stu-id="2c842-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="2c842-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2c842-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="2c842-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c842-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c842-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c842-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c842-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="2c842-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="2c842-111">Os membros **itemOld** e **itemNew** contêm informações válidas sobre o item selecionado no momento e o item selecionado recentemente.</span><span class="sxs-lookup"><span data-stu-id="2c842-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="2c842-112">O membro de **ação** indica se uma ação de mouse ou teclado está fazendo com que a seleção seja alterada.</span><span class="sxs-lookup"><span data-stu-id="2c842-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="2c842-113">Para obter uma lista de valores possíveis, consulte a descrição do código de notificação [TVN \_ SELCHANGED](tvn-selchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="2c842-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c842-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c842-114">Return value</span></span>

<span data-ttu-id="2c842-115">Retorna **true** para impedir que a seleção seja alterada.</span><span class="sxs-lookup"><span data-stu-id="2c842-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c842-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c842-116">Remarks</span></span>

<span data-ttu-id="2c842-117">Ao responder a esse código de notificação, os aplicativos não devem excluir os itens que estão recebendo ou perdendo a seleção.</span><span class="sxs-lookup"><span data-stu-id="2c842-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c842-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c842-118">Requirements</span></span>



| <span data-ttu-id="2c842-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c842-119">Requirement</span></span> | <span data-ttu-id="2c842-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2c842-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c842-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c842-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2c842-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c842-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c842-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c842-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2c842-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c842-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c842-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c842-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c842-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c842-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2c842-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2c842-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2c842-128">**TVN \_ SELCHANGINGW** (Unicode) e **TVN \_ SELCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c842-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





