---
title: HDN_TRACK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário está arrastando um divisor no controle de cabeçalho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824567"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="50601-105">Código de notificação do HDN \_ Track</span><span class="sxs-lookup"><span data-stu-id="50601-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="50601-106">Notifica uma janela pai do controle de cabeçalho que o usuário está arrastando um divisor no controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="50601-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="50601-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="50601-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="50601-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50601-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50601-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50601-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50601-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item cujo divisor está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="50601-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50601-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50601-111">Return value</span></span>

<span data-ttu-id="50601-112">Retorna **false** para continuar acompanhando o divisor ou **verdadeiro** para o rastreamento final.</span><span class="sxs-lookup"><span data-stu-id="50601-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="50601-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50601-113">Requirements</span></span>



| <span data-ttu-id="50601-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50601-114">Requirement</span></span> | <span data-ttu-id="50601-115">Valor</span><span class="sxs-lookup"><span data-stu-id="50601-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50601-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50601-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50601-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50601-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50601-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50601-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50601-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50601-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50601-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50601-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="50601-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50601-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="50601-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="50601-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="50601-123">**HDN \_ TRACKW** (Unicode) e **HDN \_ tracka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="50601-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 





