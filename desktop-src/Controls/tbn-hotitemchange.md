---
title: TBN_HOTITEMCHANGE código de notificação (commctrl. h)
description: Enviado por um controle Toolbar quando o item quente (realçado) é alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644247"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="b449a-105">Código de notificação do TBN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="b449a-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="b449a-106">Enviado por um controle Toolbar quando o item quente (realçado) é alterado.</span><span class="sxs-lookup"><span data-stu-id="b449a-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="b449a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b449a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b449a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b449a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b449a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b449a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b449a-110">Ponteiro para uma estrutura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="b449a-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b449a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b449a-111">Return value</span></span>

<span data-ttu-id="b449a-112">Retorna zero para permitir que o item seja realçado ou seja diferente de zero para impedir que o item seja realçado.</span><span class="sxs-lookup"><span data-stu-id="b449a-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="b449a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b449a-113">Requirements</span></span>



| <span data-ttu-id="b449a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b449a-114">Requirement</span></span> | <span data-ttu-id="b449a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b449a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b449a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b449a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b449a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b449a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b449a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b449a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b449a-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b449a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b449a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b449a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b449a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b449a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





