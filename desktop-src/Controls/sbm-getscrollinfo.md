---
title: Mensagem de SBM_GETSCROLLINFO (WinUser. h)
description: A \_ mensagem SBM GETSCROLLINFO é enviada para recuperar os parâmetros de uma barra de rolagem.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Controles de SBM_GETSCROLLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753789"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="9554d-104">\_Mensagem SBM GETSCROLLINFO</span><span class="sxs-lookup"><span data-stu-id="9554d-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="9554d-105">A mensagem **SBM \_ GETSCROLLINFO** é enviada para recuperar os parâmetros de uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="9554d-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="9554d-106">Os aplicativos não devem enviar essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="9554d-106">Applications should not send this message directly.</span></span> <span data-ttu-id="9554d-107">Em vez disso, eles devem usar a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="9554d-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="9554d-108">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9554d-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="9554d-109">Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollInfo** funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="9554d-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="9554d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9554d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9554d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9554d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9554d-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="9554d-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9554d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9554d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9554d-114">Ponteiro para uma estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="9554d-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="9554d-115">Antes de chamar [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), defina o membro **cbSize** da estrutura como **sizeof**(**SCROLLINFO**) e defina o membro **fMask** para especificar os parâmetros da barra de rolagem a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="9554d-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="9554d-116">Antes de retornar, a mensagem copia os parâmetros especificados para os membros apropriados da estrutura.</span><span class="sxs-lookup"><span data-stu-id="9554d-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="9554d-117">O membro **fMask** pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9554d-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="9554d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9554d-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="9554d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="9554d-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="9554d-120"><dt>**SIF \_ todos**</dt></span><span class="sxs-lookup"><span data-stu-id="9554d-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="9554d-121">Combinação de \_ Page sif, Sif \_ POS, Sif \_ Range e sif \_ TRACKPOS.</span><span class="sxs-lookup"><span data-stu-id="9554d-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="9554d-122"><dt>**\_página sif**</dt></span><span class="sxs-lookup"><span data-stu-id="9554d-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="9554d-123">Copia a página de rolagem para o membro Nconfiguração.</span><span class="sxs-lookup"><span data-stu-id="9554d-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="9554d-124"><dt>**POS do SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9554d-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="9554d-125">Copia a posição de rolagem para o membro nPos.</span><span class="sxs-lookup"><span data-stu-id="9554d-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="9554d-126"><dt>**intervalo do SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9554d-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="9554d-127">Copia o intervalo de rolagem para os membros Nmín e Nmáx.</span><span class="sxs-lookup"><span data-stu-id="9554d-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="9554d-128"><dt>**\_TRACKPOS sif**</dt></span><span class="sxs-lookup"><span data-stu-id="9554d-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="9554d-129">Copia a posição de controle da caixa de rolagem atual para o membro nTrackPos.</span><span class="sxs-lookup"><span data-stu-id="9554d-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9554d-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9554d-130">Return value</span></span>

<span data-ttu-id="9554d-131">Se a mensagem tiver recuperado quaisquer valores, o valor de retorno será **true**; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="9554d-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9554d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="9554d-132">Remarks</span></span>

<span data-ttu-id="9554d-133">As mensagens que indicam a posição da barra de rolagem, o [**WM \_ HSCROLL**](wm-hscroll.md) e o [**WM \_ VSCROLL**](wm-vscroll.md), fornecem apenas 16 bits de dados de posição.</span><span class="sxs-lookup"><span data-stu-id="9554d-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="9554d-134">No entanto, a estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada por **SBM \_ GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornece 32 bits de dados de posição da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="9554d-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="9554d-135">Você pode usar essas mensagens e funções durante o processamento das mensagens do **WM \_ HSCROLL** ou do **WM \_ VSCROLL** para obter dados de posição da barra de rolagem de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9554d-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="9554d-136">Para obter a posição de 32 bits da caixa de rolagem (Thumb) durante um \_ código de solicitação do SB THUMBTRACK em uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) , envie **SBM \_ GETSCROLLINFO** com o valor de TRACKPOS do SIF \_ no membro **fMask** da estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="9554d-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="9554d-137">A mensagem retorna a posição de rastreamento da caixa de rolagem no membro **nTrackPos** da estrutura **SCROLLINFO** .</span><span class="sxs-lookup"><span data-stu-id="9554d-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="9554d-138">Isso permite que você obtenha a posição da caixa de rolagem à medida que o usuário a move.</span><span class="sxs-lookup"><span data-stu-id="9554d-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="9554d-139">Como alternativa, você pode usar a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para obter as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="9554d-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9554d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9554d-140">Requirements</span></span>



| <span data-ttu-id="9554d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9554d-141">Requirement</span></span> | <span data-ttu-id="9554d-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9554d-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9554d-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9554d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9554d-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9554d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9554d-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9554d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9554d-146">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9554d-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9554d-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9554d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9554d-148"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9554d-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9554d-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9554d-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="9554d-150">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9554d-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9554d-151">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9554d-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="9554d-152">**SBM \_ SETSCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="9554d-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="9554d-153">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="9554d-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="9554d-154">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9554d-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

