---
title: LVN_ODSTATECHANGED código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o estado de um item ou intervalo de itens foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644912"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="429f5-105">Código de notificação do LVN \_ ODSTATECHANGED</span><span class="sxs-lookup"><span data-stu-id="429f5-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="429f5-106">Enviado por um controle de exibição de lista quando o estado de um item ou intervalo de itens foi alterado.</span><span class="sxs-lookup"><span data-stu-id="429f5-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="429f5-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="429f5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="429f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="429f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="429f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="429f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="429f5-110">Ponteiro para uma estrutura [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) que contém informações sobre o item ou itens que foram alterados.</span><span class="sxs-lookup"><span data-stu-id="429f5-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="429f5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="429f5-111">Return value</span></span>

<span data-ttu-id="429f5-112">O aplicativo que recebe esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="429f5-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="429f5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="429f5-113">Requirements</span></span>



| <span data-ttu-id="429f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="429f5-114">Requirement</span></span> | <span data-ttu-id="429f5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="429f5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="429f5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="429f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="429f5-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="429f5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="429f5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="429f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="429f5-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="429f5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="429f5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="429f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="429f5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="429f5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





