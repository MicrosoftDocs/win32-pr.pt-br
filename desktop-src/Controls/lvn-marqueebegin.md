---
title: LVN_MARQUEEBEGIN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma seleção de caixa delimitadora (letreiro) foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756236"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="6a8cc-105">Código de notificação do LVN \_ MARQUEEBEGIN</span><span class="sxs-lookup"><span data-stu-id="6a8cc-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="6a8cc-106">Notifica uma janela pai do controle de exibição de lista que uma seleção de caixa delimitadora (letreiro) foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="6a8cc-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="6a8cc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6a8cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6a8cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a8cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a8cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a8cc-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="6a8cc-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a8cc-111">Return value</span></span>

<span data-ttu-id="6a8cc-112">Para aceitar o código de notificação, retorne zero.</span><span class="sxs-lookup"><span data-stu-id="6a8cc-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="6a8cc-113">Para encerrar a seleção da caixa delimitadora, retorne diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6a8cc-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a8cc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a8cc-114">Remarks</span></span>

<span data-ttu-id="6a8cc-115">Uma *seleção de caixa delimitadora* é o processo de clicar na área do cliente da janela de exibição de lista e arrastar para selecionar vários itens simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="6a8cc-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a8cc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a8cc-116">Requirements</span></span>



| <span data-ttu-id="6a8cc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a8cc-117">Requirement</span></span> | <span data-ttu-id="6a8cc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6a8cc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8cc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a8cc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8cc-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a8cc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a8cc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a8cc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8cc-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a8cc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a8cc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a8cc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a8cc-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a8cc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





