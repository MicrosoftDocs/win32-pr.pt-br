---
title: Mensagem de LB_GETHORIZONTALEXTENT (WinUser. h)
description: Obtém a largura, em pixels, que uma caixa de listagem pode ser rolada horizontalmente (a largura rolável) se a caixa de listagem tiver uma barra de rolagem horizontal.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Controles de LB_GETHORIZONTALEXTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919087"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="24fca-104">GETHORIZONTALEXTENT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="24fca-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="24fca-105">Obtém a largura, em pixels, que uma caixa de listagem pode ser rolada horizontalmente (a largura rolável) se a caixa de listagem tiver uma barra de rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="24fca-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="24fca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24fca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24fca-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24fca-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24fca-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="24fca-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="24fca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24fca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24fca-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="24fca-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24fca-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24fca-111">Return value</span></span>

<span data-ttu-id="24fca-112">O valor de retorno é a largura rolável, em pixels, da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="24fca-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="24fca-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="24fca-113">Remarks</span></span>

<span data-ttu-id="24fca-114">Para responder à mensagem **\_ GETHORIZONTALEXTENT de lb** , a caixa de listagem deve ter sido definida com o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="24fca-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="24fca-115">Se o aplicativo não definir a extensão horizontal da caixa de listagem (usando [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), a extensão horizontal padrão será zero.</span><span class="sxs-lookup"><span data-stu-id="24fca-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="24fca-116">Observe que a caixa de listagem não atualiza sua extensão horizontal dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="24fca-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="24fca-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24fca-117">Requirements</span></span>



| <span data-ttu-id="24fca-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24fca-118">Requirement</span></span> | <span data-ttu-id="24fca-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24fca-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24fca-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24fca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24fca-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24fca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24fca-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24fca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24fca-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24fca-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24fca-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24fca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24fca-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24fca-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24fca-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="24fca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24fca-127">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="24fca-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

