---
title: Mensagem de HDM_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtém o retângulo delimitador do botão de divisão para um item de cabeçalho com o estilo HDF \_ SPLITBUTTON. Envie essa mensagem explicitamente ou usando a \_ macro GetItemDropDownRect do cabeçalho.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Controles de HDM_GETITEMDROPDOWNRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009400"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="6bfb8-105">\_Mensagem HDM GETITEMDROPDOWNRECT</span><span class="sxs-lookup"><span data-stu-id="6bfb8-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="6bfb8-106">Obtém o retângulo delimitador do botão de divisão para um item de cabeçalho com o estilo **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="6bfb8-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetItemDropDownRect do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .</span><span class="sxs-lookup"><span data-stu-id="6bfb8-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bfb8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bfb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb8-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bfb8-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfb8-110">O índice de base zero do item de controle de cabeçalho para o qual recuperar o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb8-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6bfb8-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfb8-112">Um ponteiro para uma estrutura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recebe as informações do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="6bfb8-113">O remetente da mensagem é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="6bfb8-114">As coordenadas retornadas na estrutura RECT são expressas em relação ao pai do controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bfb8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bfb8-115">Return value</span></span>

<span data-ttu-id="6bfb8-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bfb8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bfb8-117">Remarks</span></span>

<span data-ttu-id="6bfb8-118">O item de cabeçalho deve ter o estilo **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="6bfb8-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bfb8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bfb8-119">Requirements</span></span>



| <span data-ttu-id="6bfb8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bfb8-120">Requirement</span></span> | <span data-ttu-id="6bfb8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6bfb8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfb8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bfb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6bfb8-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bfb8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6bfb8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bfb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6bfb8-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6bfb8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bfb8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bfb8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bfb8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bfb8-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfb8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bfb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfb8-129">Sobre controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6bfb8-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





