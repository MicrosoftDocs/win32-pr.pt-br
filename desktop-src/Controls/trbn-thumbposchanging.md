---
title: TRBN_THUMBPOSCHANGING código de notificação (commctrl. h)
description: Notifica que a posição do Thumb em um TrackBar está sendo alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930397"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="46e0d-105">Código de notificação do TRBN \_ THUMBPOSCHANGING</span><span class="sxs-lookup"><span data-stu-id="46e0d-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="46e0d-106">Notifica que a posição do Thumb em um TrackBar está sendo alterada.</span><span class="sxs-lookup"><span data-stu-id="46e0d-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="46e0d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="46e0d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="46e0d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46e0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e0d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46e0d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46e0d-110">Ponteiro para uma estrutura [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) .</span><span class="sxs-lookup"><span data-stu-id="46e0d-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="46e0d-111">O chamador é responsável por alocar essa estrutura e definir seus membros, incluindo os membros da estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida.</span><span class="sxs-lookup"><span data-stu-id="46e0d-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e0d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46e0d-112">Return value</span></span>

<span data-ttu-id="46e0d-113">Retornar **true** para impedir que o Thumb se mova para a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="46e0d-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e0d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="46e0d-114">Remarks</span></span>

<span data-ttu-id="46e0d-115">Envie essa notificação para clientes que não escutam mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="46e0d-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e0d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e0d-116">Requirements</span></span>



| <span data-ttu-id="46e0d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e0d-117">Requirement</span></span> | <span data-ttu-id="46e0d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="46e0d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46e0d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46e0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46e0d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46e0d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46e0d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46e0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46e0d-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46e0d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46e0d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46e0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46e0d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46e0d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





