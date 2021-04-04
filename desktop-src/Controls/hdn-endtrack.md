---
title: HDN_ENDTRACK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário terminou de arrastar um divisor. Esse código de notificação é enviado na forma de uma \_ mensagem de notificação do WM.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008942"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="ae6a0-105">Código de notificação do HDN \_ ENDtrack</span><span class="sxs-lookup"><span data-stu-id="ae6a0-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="ae6a0-106">Notifica uma janela pai do controle de cabeçalho que o usuário terminou de arrastar um divisor.</span><span class="sxs-lookup"><span data-stu-id="ae6a0-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="ae6a0-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6a0-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ae6a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae6a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae6a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae6a0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae6a0-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item cujo divisor foi arrastado.</span><span class="sxs-lookup"><span data-stu-id="ae6a0-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae6a0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae6a0-111">Return value</span></span>

<span data-ttu-id="ae6a0-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ae6a0-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6a0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6a0-113">Requirements</span></span>



| <span data-ttu-id="ae6a0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6a0-114">Requirement</span></span> | <span data-ttu-id="ae6a0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ae6a0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6a0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6a0-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae6a0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae6a0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6a0-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae6a0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae6a0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae6a0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae6a0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a0-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ae6a0-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ae6a0-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ae6a0-123">**HDN \_ ENDTRACKW** (Unicode) e **HDN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ae6a0-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 





