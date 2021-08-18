---
title: 'Funções de entrada do mouse '
description: 'Funções de entrada do mouse '
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9b6abb4283ce4101b2e22c36653500db8109a0b8efbc01f9f3affe20c367a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717376"
---
# <a name="mouse-input-functions"></a>Funções de entrada do mouse 


## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br/></td>
<td>Posta mensagens quando o ponteiro do mouse sai de uma janela ou focaliza uma janela por um período de tempo especificado. Essa função chama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> se existir, caso contrário, a emulará.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a><br/></td>
<td>Captura o mouse e controla seu movimento até que o usuário libere o botão esquerdo, pressione a tecla ESC ou mova o mouse para fora do retângulo de arrastar em volta do ponto especificado. A largura e a altura do retângulo de arrastar são especificadas pelo <strong>SM_CXDRAG</strong> e <strong>SM_CYDRAG</strong> valores retornados pela função <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br/></td>
<td>Recupera um identificador para a janela (se houver) que capturou o mouse. Somente uma janela por vez pode capturar o mouse; essa janela recebe a entrada do mouse, quer o cursor esteja ou não dentro de suas bordas. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a><br/></td>
<td>Recupera o tempo de clique duplo atual para o mouse. Um clique duplo é uma série de dois cliques do botão do mouse, o segundo ocorrendo dentro de um período especificado após o primeiro. O tempo de clique duplo é o número máximo de milissegundos que podem ocorrer entre o primeiro e o segundo clique de um clique duplo. O tempo máximo de clique duplo é de 5000 milissegundos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a><br/></td>
<td>Recupera um histórico de até 64 coordenadas anteriores do mouse ou da caneta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br/></td>
<td>A função <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> sintetiza os cliques do mouse e do botão.<br/>
<blockquote>
[!Note]<br />
Esta função foi substituída. Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> em vez disso.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a><br/></td>
<td>Libera a captura do mouse de uma janela no thread atual e restaura o processamento de entrada normal do mouse. Uma janela que capturou o mouse recebe todas as entradas do mouse, independentemente da posição do cursor, exceto quando um botão do mouse é clicado enquanto o ponto de acesso do cursor está na janela de outro thread. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br/></td>
<td>Define a captura do mouse para a janela especificada pertencente ao thread atual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>Setdoubleclicktime</strong></a><br/></td>
<td>Define o tempo de clique duplo para o mouse. Um clique duplo é uma série de dois cliques de um botão do mouse, o segundo ocorrendo dentro de um período especificado após o primeiro. O tempo de clique duplo é o número máximo de milissegundos que podem ocorrer entre o primeiro e o segundo cliques de um clique duplo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a><br/></td>
<td>Reverte ou restaura o significado dos botões esquerdo e direito do mouse. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br/></td>
<td>Posta mensagens quando o ponteiro do mouse sai de uma janela ou focaliza uma janela por um período de tempo especificado.<br/>
<blockquote>
[!Note]<br />
A função <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> chama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> se existir, caso contrário <strong>_TrackMouseEvent</strong> emula <strong>TrackMouseEvent</strong>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

