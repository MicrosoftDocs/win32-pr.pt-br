---
title: Mensagem de HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtém o item em um controle de cabeçalho que tem o foco. Envie essa mensagem explicitamente ou usando a \_ macro GetFocusedItem do cabeçalho.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Controles de HDM_GETFOCUSEDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455436"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="a3f84-105">\_Mensagem HDM GETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="a3f84-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="a3f84-106">Obtém o item em um controle de cabeçalho que tem o foco.</span><span class="sxs-lookup"><span data-stu-id="a3f84-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="a3f84-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetFocusedItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="a3f84-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3f84-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3f84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f84-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3f84-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a3f84-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="a3f84-110">Not used.</span></span> <span data-ttu-id="a3f84-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a3f84-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a3f84-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3f84-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a3f84-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="a3f84-113">Not used.</span></span> <span data-ttu-id="a3f84-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a3f84-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f84-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3f84-115">Return value</span></span>

<span data-ttu-id="a3f84-116">Retorna o índice do item em foco.</span><span class="sxs-lookup"><span data-stu-id="a3f84-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f84-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3f84-117">Requirements</span></span>



| <span data-ttu-id="a3f84-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f84-118">Requirement</span></span> | <span data-ttu-id="a3f84-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a3f84-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f84-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3f84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f84-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3f84-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3f84-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3f84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f84-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3f84-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3f84-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3f84-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f84-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f84-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f84-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3f84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f84-127">Sobre controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a3f84-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





