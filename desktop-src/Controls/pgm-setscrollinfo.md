---
title: Mensagem de PGM_SETSCROLLINFO (commctrl. h)
description: Define os parâmetros de rolagem do controle de pager, incluindo o valor de tempo limite, as linhas por tempo limite e os pixels por linha. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetScrollInfo do pager.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Controles de PGM_SETSCROLLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824335"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="61cba-105">\_Mensagem SETSCROLLINFO do PGM</span><span class="sxs-lookup"><span data-stu-id="61cba-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="61cba-106">\[Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="61cba-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="61cba-107">Essa mensagem pode não ter suporte em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61cba-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="61cba-108">Define os parâmetros de rolagem do controle de pager, incluindo o valor de tempo limite, as linhas por tempo limite e os pixels por linha.</span><span class="sxs-lookup"><span data-stu-id="61cba-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="61cba-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetScrollInfo do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="61cba-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61cba-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61cba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cba-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61cba-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61cba-112">Um **uint** que especifica o valor de tempo limite para a rolagem, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="61cba-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61cba-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61cba-114">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **uint** que especifica o número de linhas a rolar por tempo limite.</span><span class="sxs-lookup"><span data-stu-id="61cba-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="61cba-115">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **uint** que especifica o número de pixels por linha.</span><span class="sxs-lookup"><span data-stu-id="61cba-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cba-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61cba-116">Return value</span></span>

<span data-ttu-id="61cba-117">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="61cba-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="61cba-118">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="61cba-118">Security Considerations</span></span>

<span data-ttu-id="61cba-119">O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="61cba-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="61cba-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="61cba-120">Remarks</span></span>

<span data-ttu-id="61cba-121">O valor de tempo limite *wParam* controla a taxa na qual o controle de pager gera eventos de rolagem quando o controle capturou a entrada do mouse e o botão esquerdo do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="61cba-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="61cba-122">Valores menores resultam em rolagem mais rápida; valores maiores resultam em uma rolagem mais lenta.</span><span class="sxs-lookup"><span data-stu-id="61cba-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="61cba-123">O valor padrão é um oitavo do tempo de clique duplo.</span><span class="sxs-lookup"><span data-stu-id="61cba-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="61cba-124">Para obter mais informações, consulte [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span><span class="sxs-lookup"><span data-stu-id="61cba-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="61cba-125">Por padrão, com cada evento de rolagem, o controle de pager rola um valor igual à largura ou altura inteira do controle, dependendo se o controle de pager tem uma orientação horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="61cba-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="61cba-126">Os valores em *lParam* são usados para substituir o valor de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="61cba-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="61cba-127">Se forem fornecidos valores diferentes de zero, o valor de rolagem será o produto dos dois valores (LOWORD (*lParam*) \* HIWORD (*lParam*)).</span><span class="sxs-lookup"><span data-stu-id="61cba-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="61cba-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61cba-128">Requirements</span></span>



| <span data-ttu-id="61cba-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cba-129">Requirement</span></span> | <span data-ttu-id="61cba-130">Valor</span><span class="sxs-lookup"><span data-stu-id="61cba-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61cba-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cba-131">Minimum supported client</span></span><br/> | <span data-ttu-id="61cba-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61cba-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61cba-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cba-133">Minimum supported server</span></span><br/> | <span data-ttu-id="61cba-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61cba-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61cba-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61cba-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="61cba-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cba-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="61cba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cba-138">**Paginar \_ SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="61cba-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

