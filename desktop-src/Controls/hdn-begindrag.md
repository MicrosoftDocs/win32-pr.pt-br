---
title: HDN_BEGINDRAG código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho quando uma operação de arrastar começou em um de seus itens. Este código de notificação é enviado somente por controles de cabeçalho que são definidos para o estilo de DRAGDROP da HDS \_ . Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009300"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="47210-106">Código de notificação do HDN \_ BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="47210-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="47210-107">Enviado por um controle de cabeçalho quando uma operação de arrastar começou em um de seus itens.</span><span class="sxs-lookup"><span data-stu-id="47210-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="47210-108">Este código de notificação é enviado somente por controles de cabeçalho que são definidos para o estilo de [**\_ DRAGDROP da HDS**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="47210-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="47210-109">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="47210-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="47210-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47210-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47210-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47210-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47210-112">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o item de cabeçalho que está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="47210-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47210-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47210-113">Return value</span></span>

<span data-ttu-id="47210-114">Para permitir que o controle de cabeçalho gerencie automaticamente as operações de arrastar e soltar, retorne **false**.</span><span class="sxs-lookup"><span data-stu-id="47210-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="47210-115">Se o proprietário do controle estiver executando manualmente a reordenação do tipo "arrastar e soltar", retorne **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="47210-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="47210-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="47210-116">Remarks</span></span>

<span data-ttu-id="47210-117">Um controle de cabeçalho usa como padrão o gerenciamento automático da reordenação do tipo "arrastar e soltar".</span><span class="sxs-lookup"><span data-stu-id="47210-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="47210-118">Retornando **true** para indicar que o gerenciamento de arrastar e soltar externo (manual) permite que o proprietário do controle forneça serviços personalizados como parte do processo de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="47210-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="47210-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47210-119">Requirements</span></span>



| <span data-ttu-id="47210-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="47210-120">Requirement</span></span> | <span data-ttu-id="47210-121">Valor</span><span class="sxs-lookup"><span data-stu-id="47210-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47210-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47210-122">Minimum supported client</span></span><br/> | <span data-ttu-id="47210-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47210-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47210-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47210-124">Minimum supported server</span></span><br/> | <span data-ttu-id="47210-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47210-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47210-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47210-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="47210-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="47210-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





