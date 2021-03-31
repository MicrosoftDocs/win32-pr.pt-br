---
title: TVN_GETINFOTIP código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore que tem o \_ estilo INFOTIP de TVs. Esse código de notificação é enviado quando o controle está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta. O código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644838"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="7b091-106">Código de notificação do TVN \_ GETINFOTIP</span><span class="sxs-lookup"><span data-stu-id="7b091-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="7b091-107">Enviado por um controle de exibição de árvore que tem o estilo [**\_ INFOTIP de TVs**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7b091-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="7b091-108">Esse código de notificação é enviado quando o controle está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="7b091-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="7b091-109">O código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7b091-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="7b091-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b091-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b091-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b091-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b091-112">Ponteiro para uma estrutura [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="7b091-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b091-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b091-113">Return value</span></span>

<span data-ttu-id="7b091-114">O controle ignora o valor de retorno para este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="7b091-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b091-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b091-115">Remarks</span></span>

<span data-ttu-id="7b091-116">Este código de notificação é enviado somente por controles de exibição de árvore que têm o estilo de [**\_ INFOTIP de TVs**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7b091-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b091-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b091-117">Requirements</span></span>



| <span data-ttu-id="7b091-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b091-118">Requirement</span></span> | <span data-ttu-id="7b091-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7b091-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b091-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b091-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b091-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b091-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b091-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b091-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b091-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b091-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b091-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b091-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b091-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b091-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7b091-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7b091-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7b091-127">**TVN \_ GETINFOTIPW** (Unicode) e **TVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7b091-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





