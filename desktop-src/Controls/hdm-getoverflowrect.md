---
title: Mensagem de HDM_GETOVERFLOWRECT (commctrl. h)
description: Obtém o retângulo delimitador do botão de estouro quando o \_ estilo de estouro da HDS é definido no controle de cabeçalho e o botão de estouro está visível. Envie essa mensagem explicitamente ou usando a \_ macro GetOverflowRect do cabeçalho.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Controles de HDM_GETOVERFLOWRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499488"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="612c5-105">\_Mensagem HDM GETOVERFLOWRECT</span><span class="sxs-lookup"><span data-stu-id="612c5-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="612c5-106">Obtém o retângulo delimitador do botão de estouro quando o estilo de [**\_ estouro da HDS**](header-control-styles.md) é definido no controle de cabeçalho e o botão de estouro está visível.</span><span class="sxs-lookup"><span data-stu-id="612c5-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="612c5-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetOverflowRect do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .</span><span class="sxs-lookup"><span data-stu-id="612c5-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="612c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="612c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="612c5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="612c5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="612c5-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="612c5-110">Not used.</span></span> <span data-ttu-id="612c5-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="612c5-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="612c5-112">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="612c5-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="612c5-113">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as informações do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="612c5-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="612c5-114">O remetente da mensagem é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="612c5-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="612c5-115">As coordenadas retornadas na estrutura **Rect** são expressas como coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="612c5-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="612c5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="612c5-116">Return value</span></span>

<span data-ttu-id="612c5-117">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="612c5-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="612c5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="612c5-118">Remarks</span></span>

<span data-ttu-id="612c5-119">O controle de cabeçalho deve ter o estilo **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="612c5-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="612c5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="612c5-120">Requirements</span></span>



| <span data-ttu-id="612c5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="612c5-121">Requirement</span></span> | <span data-ttu-id="612c5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="612c5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="612c5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="612c5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="612c5-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="612c5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="612c5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="612c5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="612c5-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="612c5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="612c5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="612c5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="612c5-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="612c5-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="612c5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="612c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612c5-130">Sobre controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="612c5-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

