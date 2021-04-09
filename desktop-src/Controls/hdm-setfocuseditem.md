---
title: Mensagem de HDM_SETFOCUSEDITEM (commctrl. h)
description: Define o foco para um item especificado em um controle de cabeçalho. Envie essa mensagem explicitamente ou usando a \_ macro SetFocusedItem do cabeçalho.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Controles de HDM_SETFOCUSEDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086093"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="09fef-105">\_Mensagem HDM SETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="09fef-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="09fef-106">Define o foco para um item especificado em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="09fef-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="09fef-107">Envie essa mensagem explicitamente ou usando a macro [**\_ SetFocusedItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="09fef-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="09fef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09fef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09fef-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="09fef-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="09fef-110">Not used.</span></span> <span data-ttu-id="09fef-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="09fef-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="09fef-112">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09fef-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fef-113">O índice do item.</span><span class="sxs-lookup"><span data-stu-id="09fef-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fef-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09fef-114">Return value</span></span>

<span data-ttu-id="09fef-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="09fef-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fef-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fef-116">Requirements</span></span>



| <span data-ttu-id="09fef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fef-117">Requirement</span></span> | <span data-ttu-id="09fef-118">Valor</span><span class="sxs-lookup"><span data-stu-id="09fef-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09fef-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09fef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09fef-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09fef-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09fef-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09fef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09fef-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09fef-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09fef-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09fef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fef-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fef-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09fef-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="09fef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fef-126">Sobre controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="09fef-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





