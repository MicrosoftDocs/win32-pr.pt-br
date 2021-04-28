---
title: 'Funções de entrada do mouse '
description: 'Funções de entrada do mouse '
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a952a9ce90284f284b176c608228c0b852f5f4c8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112874"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="0e440-103">Funções de entrada do mouse </span><span class="sxs-lookup"><span data-stu-id="0e440-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="0e440-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0e440-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e440-105">Tópico</span><span class="sxs-lookup"><span data-stu-id="0e440-105">Topic</span></span></th>
<th><span data-ttu-id="0e440-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e440-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e440-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-108">Posta mensagens quando o ponteiro do mouse sai de uma janela ou focaliza uma janela por um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="0e440-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="0e440-109">Essa função chama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> se existir, caso contrário, a emulará.</span><span class="sxs-lookup"><span data-stu-id="0e440-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e440-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-111">Captura o mouse e controla seu movimento até que o usuário libere o botão esquerdo, pressione a tecla ESC ou mova o mouse para fora do retângulo de arrastar em volta do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="0e440-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="0e440-112">A largura e a altura do retângulo de arrastar são especificadas pelo <strong>SM_CXDRAG</strong> e <strong>SM_CYDRAG</strong> valores retornados pela função <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e440-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e440-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-114">Recupera um identificador para a janela (se houver) que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="0e440-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="0e440-115">Somente uma janela por vez pode capturar o mouse; essa janela recebe a entrada do mouse, quer o cursor esteja ou não dentro de suas bordas.</span><span class="sxs-lookup"><span data-stu-id="0e440-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e440-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-117">Recupera o tempo de clique duplo atual para o mouse.</span><span class="sxs-lookup"><span data-stu-id="0e440-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="0e440-118">Um clique duplo é uma série de dois cliques do botão do mouse, o segundo ocorrendo dentro de um período especificado após o primeiro.</span><span class="sxs-lookup"><span data-stu-id="0e440-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="0e440-119">O tempo de clique duplo é o número máximo de milissegundos que podem ocorrer entre o primeiro e o segundo clique de um clique duplo.</span><span class="sxs-lookup"><span data-stu-id="0e440-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="0e440-120">O tempo máximo de clique duplo é de 5000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="0e440-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e440-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-122">Recupera um histórico de até 64 coordenadas anteriores do mouse ou da caneta.</span><span class="sxs-lookup"><span data-stu-id="0e440-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e440-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-124">A função <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> sintetiza os cliques do mouse e do botão.</span><span class="sxs-lookup"><span data-stu-id="0e440-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e440-125">Esta função foi substituída.</span><span class="sxs-lookup"><span data-stu-id="0e440-125">This function has been superseded.</span></span> <span data-ttu-id="0e440-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0e440-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e440-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-128">Libera a captura do mouse de uma janela no thread atual e restaura o processamento de entrada normal do mouse.</span><span class="sxs-lookup"><span data-stu-id="0e440-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="0e440-129">Uma janela que capturou o mouse recebe todas as entradas do mouse, independentemente da posição do cursor, exceto quando um botão do mouse é clicado enquanto o ponto de acesso do cursor está na janela de outro thread.</span><span class="sxs-lookup"><span data-stu-id="0e440-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e440-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-131">Define a captura do mouse para a janela especificada pertencente ao thread atual.</span><span class="sxs-lookup"><span data-stu-id="0e440-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e440-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>Setdoubleclicktime</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-133">Define o tempo de clique duplo para o mouse.</span><span class="sxs-lookup"><span data-stu-id="0e440-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="0e440-134">Um clique duplo é uma série de dois cliques de um botão do mouse, o segundo ocorrendo dentro de um período especificado após o primeiro.</span><span class="sxs-lookup"><span data-stu-id="0e440-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="0e440-135">O tempo de clique duplo é o número máximo de milissegundos que podem ocorrer entre o primeiro e o segundo cliques de um clique duplo.</span><span class="sxs-lookup"><span data-stu-id="0e440-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e440-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-137">Reverte ou restaura o significado dos botões esquerdo e direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="0e440-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e440-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e440-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="0e440-139">Posta mensagens quando o ponteiro do mouse sai de uma janela ou focaliza uma janela por um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="0e440-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e440-140">A função <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> chama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> se existir, caso contrário <strong>_TrackMouseEvent</strong> emula <strong>TrackMouseEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e440-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

