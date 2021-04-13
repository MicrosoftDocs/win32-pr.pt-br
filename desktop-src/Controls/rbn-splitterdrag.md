---
title: RBN_SPLITTERDRAG código de notificação (commctrl. h)
description: Enviado por um controle rebar quando o usuário arrasta um divisor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499538"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="660f6-105">Código de notificação do RBN \_ SPLITTERDRAG</span><span class="sxs-lookup"><span data-stu-id="660f6-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="660f6-106">Enviado por um controle rebar quando o usuário arrasta um divisor.</span><span class="sxs-lookup"><span data-stu-id="660f6-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="660f6-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="660f6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="660f6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="660f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="660f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="660f6-110">Ponteiro para uma estrutura [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="660f6-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="660f6-111">Return value</span></span>

<span data-ttu-id="660f6-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="660f6-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="660f6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="660f6-113">Requirements</span></span>



| <span data-ttu-id="660f6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="660f6-114">Requirement</span></span> | <span data-ttu-id="660f6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="660f6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="660f6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="660f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="660f6-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="660f6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="660f6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="660f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="660f6-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="660f6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="660f6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="660f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="660f6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="660f6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





