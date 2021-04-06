---
title: Mensagem de SB_SETTEXT (commctrl. h)
description: Define o texto na parte especificada de uma janela de status.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Controles de SB_SETTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086018"
---
# <a name="sb_settext-message"></a><span data-ttu-id="dfbb7-104">\_Mensagem de SETtext do SB</span><span class="sxs-lookup"><span data-stu-id="dfbb7-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="dfbb7-105">Define o texto na parte especificada de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="dfbb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfbb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfbb7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfbb7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbb7-108">O [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) da palavra de ordem inferior Especifica o índice de base zero da parte a ser definida.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="dfbb7-109">Se **LOBYTE** for definido como SB \_ simpleid, a janela de status será considerada uma barra de status de modo simples; ou seja, uma barra de status com apenas uma parte.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="dfbb7-110">O [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) da palavra de ordem inferior Especifica o tipo da operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="dfbb7-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="dfbb7-112">A palavra de ordem superior de *wParam* é ignorada.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dfbb7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dfbb7-113">Value</span></span></th>
<th><span data-ttu-id="dfbb7-114">Significado</span><span class="sxs-lookup"><span data-stu-id="dfbb7-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="dfbb7-115"><dt><strong>0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfbb7-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dfbb7-116">O texto é desenhado com uma borda para aparecer menor do que o plano da janela.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="dfbb7-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfbb7-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dfbb7-118">O texto é desenhado sem bordas.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="dfbb7-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfbb7-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dfbb7-120">O texto é desenhado pela janela pai.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dfbb7-121">Uma barra de status de modo simples não dá suporte ao desenho de proprietário.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="dfbb7-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfbb7-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dfbb7-123">O texto é desenhado com uma borda para aparecer maior do que o plano da janela.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="dfbb7-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfbb7-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dfbb7-125">O texto será exibido na direção oposta ao texto na janela pai.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="dfbb7-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfbb7-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="dfbb7-127">Os caracteres de tabulação são ignorados.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="dfbb7-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfbb7-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbb7-129">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o texto a ser definido.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="dfbb7-130">Se *wParam* for SBT \_ OWNERDRAW, esse parâmetro representará 32 bits de dados.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="dfbb7-131">A janela pai deve interpretar os dados e desenhar o texto quando receber a mensagem [**\_ DRAWITEM do WM**](wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbb7-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfbb7-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfbb7-132">Return value</span></span>

<span data-ttu-id="dfbb7-133">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfbb7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfbb7-134">Remarks</span></span>

<span data-ttu-id="dfbb7-135">A mensagem invalida a parte da janela que foi alterada, fazendo com que ela exiba o novo texto quando a janela recebe a próxima mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="dfbb7-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="dfbb7-136">Texto de exibição normal do Windows da esquerda para a direita (EPD).</span><span class="sxs-lookup"><span data-stu-id="dfbb7-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="dfbb7-137">O Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que são lidos da direita para a esquerda (RTL).</span><span class="sxs-lookup"><span data-stu-id="dfbb7-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="dfbb7-138">Se SBT \_ RTLREADING for definido, a cadeia de caracteres *lParam* lerá na direção oposta do texto na janela pai.</span><span class="sxs-lookup"><span data-stu-id="dfbb7-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfbb7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfbb7-139">Requirements</span></span>



| <span data-ttu-id="dfbb7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfbb7-140">Requirement</span></span> | <span data-ttu-id="dfbb7-141">Valor</span><span class="sxs-lookup"><span data-stu-id="dfbb7-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbb7-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfbb7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbb7-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfbb7-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dfbb7-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfbb7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbb7-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfbb7-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dfbb7-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfbb7-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfbb7-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbb7-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="dfbb7-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="dfbb7-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dfbb7-149">**SB \_ SETTEXTW** (Unicode) e **SB \_ settexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dfbb7-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="dfbb7-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfbb7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbb7-151">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="dfbb7-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 

