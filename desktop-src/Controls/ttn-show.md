---
title: TTN_SHOW código de notificação (commctrl. h)
description: Notifica a janela do proprietário que um controle ToolTip está prestes a ser exibido. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918517"
---
# <a name="ttn_show-notification-code"></a><span data-ttu-id="75818-105">TTN \_ Mostrar código de notificação</span><span class="sxs-lookup"><span data-stu-id="75818-105">TTN\_SHOW notification code</span></span>

<span data-ttu-id="75818-106">Notifica a janela do proprietário que um controle ToolTip está prestes a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="75818-106">Notifies the owner window that a tooltip control is about to be displayed.</span></span> <span data-ttu-id="75818-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="75818-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="75818-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75818-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75818-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75818-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75818-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="75818-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75818-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75818-111">Return value</span></span>

<span data-ttu-id="75818-112">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="75818-112">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="75818-113">Para exibir a dica de ferramenta em seu local padrão, retorne zero.</span><span class="sxs-lookup"><span data-stu-id="75818-113">To display the tooltip in its default location, return zero.</span></span> <span data-ttu-id="75818-114">Para personalizar a posição da dica de ferramenta, reposicione a janela de dica de ferramenta com a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) e retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="75818-114">To customize the tooltip position, reposition the tooltip window with the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function and return **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="75818-115">Para versões anteriores a 4,70, não há nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="75818-115">For versions earlier than 4.70, there is no return value.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="75818-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="75818-116">Remarks</span></span>

<span data-ttu-id="75818-117">Um retângulo de janela de dica de ferramenta é um pouco maior do que seu retângulo de exibição de texto, e sua origem é deslocada para cima e para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="75818-117">A tooltip window rectangle is somewhat larger than its text display rectangle, and its origin is offset up and to the left.</span></span> <span data-ttu-id="75818-118">Se você precisar posicionar com precisão o retângulo de exibição de texto de uma dica de ferramenta, a mensagem [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) converterá um retângulo de exibição de texto no retângulo da janela de dica de ferramenta correspondente e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="75818-118">If you need to accurately position the text display rectangle of a tooltip, the [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message converts a text display rectangle into the corresponding tooltip window rectangle and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="75818-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75818-119">Requirements</span></span>



| <span data-ttu-id="75818-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="75818-120">Requirement</span></span> | <span data-ttu-id="75818-121">Valor</span><span class="sxs-lookup"><span data-stu-id="75818-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75818-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75818-122">Minimum supported client</span></span><br/> | <span data-ttu-id="75818-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75818-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75818-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75818-124">Minimum supported server</span></span><br/> | <span data-ttu-id="75818-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75818-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75818-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75818-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="75818-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75818-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

