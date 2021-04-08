---
title: HDN_BEGINTRACK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário começou a arrastar um divisor no controle (ou seja, o usuário pressionou o botão esquerdo do mouse enquanto o cursor do mouse está sobre um divisor no controle de cabeçalho).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086557"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="ca4da-104">Código de notificação do HDN \_ BEGINTRACK</span><span class="sxs-lookup"><span data-stu-id="ca4da-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="ca4da-105">Notifica uma janela pai do controle de cabeçalho que o usuário começou a arrastar um divisor no controle (ou seja, o usuário pressionou o botão esquerdo do mouse enquanto o cursor do mouse está sobre um divisor no controle de cabeçalho).</span><span class="sxs-lookup"><span data-stu-id="ca4da-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="ca4da-106">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ca4da-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ca4da-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca4da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca4da-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca4da-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca4da-109">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item cujo divisor deve ser arrastado.</span><span class="sxs-lookup"><span data-stu-id="ca4da-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca4da-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca4da-110">Return value</span></span>

<span data-ttu-id="ca4da-111">Retorna **false** para permitir o acompanhamento do divisor ou **true** para impedir o acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="ca4da-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4da-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca4da-112">Requirements</span></span>



| <span data-ttu-id="ca4da-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca4da-113">Requirement</span></span> | <span data-ttu-id="ca4da-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ca4da-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4da-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca4da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ca4da-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca4da-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca4da-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca4da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ca4da-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca4da-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca4da-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca4da-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca4da-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca4da-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ca4da-121">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ca4da-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ca4da-122">**HDN \_ BEGINTRACKW** (Unicode) e **HDN \_ BEGINTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ca4da-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 





