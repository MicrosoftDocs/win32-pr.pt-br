---
title: HDN_ENDDRAG código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho quando uma operação de arrastar termina em um de seus itens. Esse código de notificação é enviado como uma \_ mensagem de notificação do WM. Somente controles de cabeçalho que são definidos para o \_ estilo HDS DRAGDROP enviam este código de notificação.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456057"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="c3bb0-106">Código de notificação do HDN \_ ENDarraste</span><span class="sxs-lookup"><span data-stu-id="c3bb0-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="c3bb0-107">Enviado por um controle de cabeçalho quando uma operação de arrastar termina em um de seus itens.</span><span class="sxs-lookup"><span data-stu-id="c3bb0-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="c3bb0-108">Esse código de notificação é enviado como uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c3bb0-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="c3bb0-109">Somente controles de cabeçalho que são definidos para o estilo [**HDS \_ DRAGDROP**](header-control-styles.md) enviam este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="c3bb0-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c3bb0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3bb0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3bb0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3bb0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3bb0-112">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o item de cabeçalho que estava sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="c3bb0-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3bb0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3bb0-113">Return value</span></span>

<span data-ttu-id="c3bb0-114">Para permitir que o controle Coloque e reordene automaticamente o item, retorne **false**.</span><span class="sxs-lookup"><span data-stu-id="c3bb0-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="c3bb0-115">Para impedir que o item seja colocado, retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="c3bb0-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3bb0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3bb0-116">Remarks</span></span>

<span data-ttu-id="c3bb0-117">Se o proprietário estiver executando o gerenciamento de arrastar e soltar externo (manual), ele deverá retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="c3bb0-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="c3bb0-118">Em seguida, o proprietário deve reordenar os itens de cabeçalho manualmente enviando [**HDM \_ SETITEM**](hdm-setitem.md) ou [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).</span><span class="sxs-lookup"><span data-stu-id="c3bb0-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bb0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3bb0-119">Requirements</span></span>



| <span data-ttu-id="c3bb0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3bb0-120">Requirement</span></span> | <span data-ttu-id="c3bb0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c3bb0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3bb0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3bb0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3bb0-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3bb0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3bb0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3bb0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3bb0-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3bb0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3bb0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3bb0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3bb0-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3bb0-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





