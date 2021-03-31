---
title: Barra de rolagem simples
description: Esta seção contém informações sobre os elementos de programação usados para controlar barras de rolagem simples.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822417"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="ef344-103">Barra de rolagem simples</span><span class="sxs-lookup"><span data-stu-id="ef344-103">Flat Scroll Bar</span></span>

<span data-ttu-id="ef344-104">Esta seção contém informações sobre os elementos de programação usados para controlar barras de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="ef344-105">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="ef344-105">Overviews</span></span>



| <span data-ttu-id="ef344-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="ef344-106">Topic</span></span>                                    | <span data-ttu-id="ef344-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="ef344-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef344-108">Barras de rolagem simples</span><span class="sxs-lookup"><span data-stu-id="ef344-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="ef344-109">O Microsoft Internet Explorer 4,0 introduziu uma nova tecnologia Visual chamada barras de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="ef344-110">Funcionalmente, barras de rolagem simples se comportam exatamente como barras de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="ef344-111">A diferença é que você pode personalizar sua aparência para uma extensão maior do que as barras de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="ef344-112">Funções</span><span class="sxs-lookup"><span data-stu-id="ef344-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef344-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="ef344-113">Topic</span></span></th>
<th><span data-ttu-id="ef344-114">Sumário</span><span class="sxs-lookup"><span data-stu-id="ef344-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef344-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="ef344-116">Habilita ou desabilita um ou ambos os botões de direção da barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="ef344-117">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef344-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="ef344-119">Obtém as informações de uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="ef344-120">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef344-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="ef344-122">Obtém a posição do polegar em uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="ef344-123">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef344-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="ef344-125">Obtém as propriedades de uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="ef344-126">Essa função também pode ser usada para determinar se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> foi chamado para esta janela.</span><span class="sxs-lookup"><span data-stu-id="ef344-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef344-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="ef344-128">Obtém as propriedades de uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="ef344-129">Essa função também pode ser usada para determinar se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> foi chamado para esta janela.</span><span class="sxs-lookup"><span data-stu-id="ef344-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ef344-130">Isso é idêntico ao <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ef344-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef344-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="ef344-132">Obtém o intervalo de rolagem de uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="ef344-133">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef344-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="ef344-135">Define as informações para uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="ef344-136">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef344-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="ef344-138">Define a posição atual do Thumb em uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="ef344-139">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef344-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="ef344-141">Define as propriedades de uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef344-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="ef344-143">Define o intervalo de rolagem de uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="ef344-144">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef344-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="ef344-146">Mostra ou oculta uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="ef344-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="ef344-147">Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função de lista de <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>rolagem</strong></a> padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef344-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="ef344-149">Inicializa barras de rolagem simples para uma janela específica.</span><span class="sxs-lookup"><span data-stu-id="ef344-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef344-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef344-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="ef344-151">Não inicializa barras de rolagem simples para uma janela específica.</span><span class="sxs-lookup"><span data-stu-id="ef344-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="ef344-152">A janela especificada será revertida para as barras de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="ef344-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 





