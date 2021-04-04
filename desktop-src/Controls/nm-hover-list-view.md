---
title: Código de notificação de NM_HOVER (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o mouse passa sobre um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- NM_HOVER de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824160"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="77381-105">\_Código de notificação de foco de nm (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="77381-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="77381-106">Enviado por um controle de exibição de lista quando o mouse passa sobre um item.</span><span class="sxs-lookup"><span data-stu-id="77381-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="77381-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="77381-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="77381-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77381-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77381-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77381-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77381-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="77381-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77381-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77381-111">Return value</span></span>

<span data-ttu-id="77381-112">Retornar zero para permitir que o modo de exibição de lista processe o foco normalmente ou diferente de zero para impedir que o foco seja processado.</span><span class="sxs-lookup"><span data-stu-id="77381-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="77381-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77381-113">Requirements</span></span>



| <span data-ttu-id="77381-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77381-114">Requirement</span></span> | <span data-ttu-id="77381-115">Valor</span><span class="sxs-lookup"><span data-stu-id="77381-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77381-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77381-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77381-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77381-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77381-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77381-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77381-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77381-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77381-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77381-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="77381-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77381-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





