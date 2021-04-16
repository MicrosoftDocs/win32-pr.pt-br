---
title: Mensagem de SBM_SETSCROLLINFO (WinUser. h)
description: A \_ mensagem SBM SETSCROLLINFO é enviada para definir os parâmetros de uma barra de rolagem.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- Controles de SBM_SETSCROLLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753788"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="bd387-104">\_Mensagem SBM SETSCROLLINFO</span><span class="sxs-lookup"><span data-stu-id="bd387-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="bd387-105">A mensagem **SBM \_ SETSCROLLINFO** é enviada para definir os parâmetros de uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="bd387-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="bd387-106">Os aplicativos não devem enviar essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="bd387-106">Applications should not send this message directly.</span></span> <span data-ttu-id="bd387-107">Em vez disso, eles devem usar a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="bd387-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="bd387-108">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bd387-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="bd387-109">Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollInfo** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="bd387-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd387-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd387-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd387-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd387-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd387-112">Especifica se a barra de rolagem é redesenhada para refletir a nova posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="bd387-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="bd387-113">Se esse parâmetro for **true**, a barra de rolagem será redesenhada.</span><span class="sxs-lookup"><span data-stu-id="bd387-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="bd387-114">Se for **false**, a barra de rolagem não será redesenhada.</span><span class="sxs-lookup"><span data-stu-id="bd387-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="bd387-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd387-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd387-116">Ponteiro para uma estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="bd387-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="bd387-117">Antes de chamar [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), defina o membro **cbSize** da estrutura como **sizeof**(**SCROLLINFO**), defina o membro **fMask** para indicar os parâmetros a serem definidos e especifique os novos valores de parâmetro nos membros apropriados.</span><span class="sxs-lookup"><span data-stu-id="bd387-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="bd387-118">O membro **fMask** pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd387-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="bd387-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bd387-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="bd387-120">Significado</span><span class="sxs-lookup"><span data-stu-id="bd387-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="bd387-121"><dt>**\_DISABLENOSCROLL sif**</dt></span><span class="sxs-lookup"><span data-stu-id="bd387-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="bd387-122">Desabilita a barra de rolagem em vez de removê-la, se os novos parâmetros da barra de rolagem tornarem a barra de rolagem desnecessária.</span><span class="sxs-lookup"><span data-stu-id="bd387-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="bd387-123"><dt>**\_página sif**</dt></span><span class="sxs-lookup"><span data-stu-id="bd387-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="bd387-124">Define a página de rolagem para o valor especificado no membro **nconfiguração** .</span><span class="sxs-lookup"><span data-stu-id="bd387-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="bd387-125"><dt>**POS do SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bd387-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="bd387-126">Define a posição de rolagem para o valor especificado no membro **nPos** .</span><span class="sxs-lookup"><span data-stu-id="bd387-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="bd387-127"><dt>**intervalo do SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bd387-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="bd387-128">Define o intervalo de rolagem para o valor especificado nos membros **nmín** e **nmáx** .</span><span class="sxs-lookup"><span data-stu-id="bd387-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd387-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd387-129">Return value</span></span>

<span data-ttu-id="bd387-130">O valor de retorno é a posição atual da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="bd387-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd387-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd387-131">Remarks</span></span>

<span data-ttu-id="bd387-132">As mensagens que indicam a posição da barra de rolagem, o [**WM \_ HSCROLL**](wm-hscroll.md) e o [**WM \_ VSCROLL**](wm-vscroll.md), fornecem apenas 16 bits de dados de posição.</span><span class="sxs-lookup"><span data-stu-id="bd387-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="bd387-133">No entanto, a estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada por [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornece 32 bits de dados de posição da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="bd387-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="bd387-134">Você pode usar essas mensagens e funções durante o processamento das mensagens do **WM \_ HSCROLL** ou do **WM \_ VSCROLL** para obter dados de posição da barra de rolagem de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bd387-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd387-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd387-135">Requirements</span></span>



| <span data-ttu-id="bd387-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd387-136">Requirement</span></span> | <span data-ttu-id="bd387-137">Valor</span><span class="sxs-lookup"><span data-stu-id="bd387-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd387-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd387-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bd387-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd387-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd387-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd387-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bd387-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd387-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd387-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd387-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd387-143"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd387-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd387-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd387-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd387-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bd387-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd387-146">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="bd387-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="bd387-147">**SBM \_ GETSCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="bd387-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="bd387-148">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="bd387-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="bd387-149">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="bd387-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

