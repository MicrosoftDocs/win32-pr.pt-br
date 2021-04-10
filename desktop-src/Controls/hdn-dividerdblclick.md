---
title: HDN_DIVIDERDBLCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou duas vezes na área divisória do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009780"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="975e1-105">Código de notificação do HDN \_ DIVIDERDBLCLICK</span><span class="sxs-lookup"><span data-stu-id="975e1-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="975e1-106">Notifica uma janela pai do controle de cabeçalho que o usuário clicou duas vezes na área divisória do controle.</span><span class="sxs-lookup"><span data-stu-id="975e1-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="975e1-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="975e1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="975e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="975e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="975e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="975e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="975e1-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item cujo divisor foi clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="975e1-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="975e1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="975e1-111">Return value</span></span>

<span data-ttu-id="975e1-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="975e1-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="975e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="975e1-113">Requirements</span></span>



| <span data-ttu-id="975e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="975e1-114">Requirement</span></span> | <span data-ttu-id="975e1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="975e1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="975e1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="975e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="975e1-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="975e1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="975e1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="975e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="975e1-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="975e1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="975e1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="975e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="975e1-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="975e1-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="975e1-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="975e1-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="975e1-123">**HDN \_ DIVIDERDBLCLICKW** (Unicode) e **HDN \_ DIVIDERDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="975e1-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 





