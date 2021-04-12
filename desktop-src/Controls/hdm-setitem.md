---
title: Mensagem de HDM_SETITEM (commctrl. h)
description: Define os atributos do item especificado em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetItem do cabeçalho.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- Controles de HDM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455663"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="93e8e-105">\_Mensagem HDM SETITEM</span><span class="sxs-lookup"><span data-stu-id="93e8e-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="93e8e-106">Define os atributos do item especificado em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="93e8e-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="93e8e-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .</span><span class="sxs-lookup"><span data-stu-id="93e8e-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="93e8e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93e8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e8e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93e8e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93e8e-110">O índice atual do item cujos atributos devem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="93e8e-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="93e8e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93e8e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93e8e-112">Um ponteiro para uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contém informações de item.</span><span class="sxs-lookup"><span data-stu-id="93e8e-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="93e8e-113">Quando essa mensagem é enviada, o membro **Mask** da estrutura deve ser definido para indicar quais atributos estão sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="93e8e-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e8e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93e8e-114">Return value</span></span>

<span data-ttu-id="93e8e-115">Retorna zero após o êxito ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="93e8e-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e8e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="93e8e-116">Remarks</span></span>

<span data-ttu-id="93e8e-117">A estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que dá suporte a essa mensagem dá suporte a informações de ordem de item e de lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="93e8e-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="93e8e-118">Ao usar esses membros, você pode controlar a ordem na qual os itens são exibidos e especificar imagens para serem exibidos com os itens.</span><span class="sxs-lookup"><span data-stu-id="93e8e-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e8e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e8e-119">Requirements</span></span>



| <span data-ttu-id="93e8e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e8e-120">Requirement</span></span> | <span data-ttu-id="93e8e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="93e8e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93e8e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e8e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="93e8e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93e8e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93e8e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e8e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="93e8e-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93e8e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93e8e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93e8e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e8e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93e8e-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="93e8e-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="93e8e-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="93e8e-129">**HDM \_ SETITEMW** (Unicode) e **HDM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="93e8e-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





