---
title: RBN_BEGINDRAG código de notificação (commctrl. h)
description: Enviado por um controle rebar quando o usuário começa a arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- RBN_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454687"
---
# <a name="rbn_begindrag-notification-code"></a><span data-ttu-id="8960c-105">Código de notificação do RBN \_ BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="8960c-105">RBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="8960c-106">Enviado por um controle rebar quando o usuário começa a arrastar uma banda.</span><span class="sxs-lookup"><span data-stu-id="8960c-106">Sent by a rebar control when the user begins dragging a band.</span></span> <span data-ttu-id="8960c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8960c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8960c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8960c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8960c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8960c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8960c-110">Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="8960c-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8960c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8960c-111">Return value</span></span>

<span data-ttu-id="8960c-112">Retorne zero para permitir que o rebar continue a operação de arrastar ou diferente de zero para anular a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="8960c-112">Return zero to allow the rebar to continue the drag operation, or nonzero to abort the drag operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8960c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8960c-113">Requirements</span></span>



| <span data-ttu-id="8960c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8960c-114">Requirement</span></span> | <span data-ttu-id="8960c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8960c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8960c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8960c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8960c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8960c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8960c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8960c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8960c-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8960c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8960c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8960c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8960c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8960c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





