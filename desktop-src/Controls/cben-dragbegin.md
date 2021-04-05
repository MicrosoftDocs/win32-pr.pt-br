---
title: CBEN_DRAGBEGIN código de notificação (commctrl. h)
description: Enviado quando o usuário começa a arrastar a imagem do item exibido na parte de edição do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086248"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="641e9-105">Código de notificação do CBEN \_ DRAGBEGIN</span><span class="sxs-lookup"><span data-stu-id="641e9-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="641e9-106">Enviado quando o usuário começa a arrastar a imagem do item exibido na parte de edição do controle.</span><span class="sxs-lookup"><span data-stu-id="641e9-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="641e9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="641e9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="641e9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="641e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="641e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="641e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="641e9-110">Um ponteiro para uma estrutura [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="641e9-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="641e9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="641e9-111">Return value</span></span>

<span data-ttu-id="641e9-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="641e9-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="641e9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="641e9-113">Remarks</span></span>

<span data-ttu-id="641e9-114">Se o aplicativo de recebimento implementar a funcionalidade de arrastar e soltar do controle, o aplicativo iniciará a operação de arrastar e soltar em resposta a este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="641e9-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="641e9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="641e9-115">Requirements</span></span>



| <span data-ttu-id="641e9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="641e9-116">Requirement</span></span> | <span data-ttu-id="641e9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="641e9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="641e9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="641e9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="641e9-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="641e9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="641e9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="641e9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="641e9-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="641e9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="641e9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="641e9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="641e9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="641e9-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="641e9-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="641e9-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="641e9-125">**CBEN \_ DRAGBEGINW** (Unicode) e **CBEN \_ DRAGBEGINA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="641e9-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





