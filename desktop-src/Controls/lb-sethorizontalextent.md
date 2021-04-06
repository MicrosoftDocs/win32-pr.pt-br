---
title: Mensagem de LB_SETHORIZONTALEXTENT (WinUser. h)
description: Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Controles de LB_SETHORIZONTALEXTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824677"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="d3e2e-104">SETHORIZONTALEXTENT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="d3e2e-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="d3e2e-105">Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).</span><span class="sxs-lookup"><span data-stu-id="d3e2e-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="d3e2e-106">Se a largura da caixa de listagem for menor que esse valor, a barra de rolagem horizontal rolará horizontalmente os itens na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="d3e2e-107">Se a largura da caixa de listagem for igual ou maior que esse valor, a barra de rolagem horizontal ficará oculta.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3e2e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3e2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e2e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3e2e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3e2e-110">Especifica o número de pixels pelos quais a caixa de listagem pode ser rolada.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="d3e2e-111">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="d3e2e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3e2e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3e2e-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e2e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3e2e-114">Return value</span></span>

<span data-ttu-id="d3e2e-115">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e2e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3e2e-116">Remarks</span></span>

<span data-ttu-id="d3e2e-117">Para responder à mensagem **\_ SETHORIZONTALEXTENT de lb** , a caixa de listagem deve ter sido definida com o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="d3e2e-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="d3e2e-118">Observe que uma caixa de listagem não atualiza sua extensão horizontal dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="d3e2e-119">Esta mensagem não tem nenhum efeito em uma caixa de listagem de várias colunas.</span><span class="sxs-lookup"><span data-stu-id="d3e2e-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e2e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3e2e-120">Requirements</span></span>



| <span data-ttu-id="d3e2e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e2e-121">Requirement</span></span> | <span data-ttu-id="d3e2e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e2e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e2e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3e2e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e2e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3e2e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3e2e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3e2e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e2e-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3e2e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3e2e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3e2e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e2e-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3e2e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e2e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3e2e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e2e-130">**\_GETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="d3e2e-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

