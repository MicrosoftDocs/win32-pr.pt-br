---
title: Mensagens
description: Os tópicos nesta seção fornecem as especificações de referência para mensagens de entrada e notificações específicas do ponteiro.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365995"
---
# <a name="messages"></a>Mensagens

Os tópicos nesta seção fornecem as especificações de referência para [mensagens de entrada e notificações](messages-and-notifications-portal.md)específicas do ponteiro.

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
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md)<br/></td>
<td>Enviado para uma janela, quando a entrada do ponteiro é detectada pela primeira vez, para determinar o destino de entrada mais provável para a [manipulação direta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal). <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Postado quando um ponteiro faz contato na área que não é do cliente de uma janela. A mensagem é direcionada para a janela sobre a qual o ponteiro faz contato. O ponteiro é capturado implicitamente na janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato. <br/> Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) é Postado na janela que capturou esse ponteiro. <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Postado quando um ponteiro que fez contato na área de não cliente de uma janela quebra o contato. A mensagem é direcionada para a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato, incluindo a notificação [<strong>WM_NCPOINTERUP</strong>] (WM-ncpointerup.MD). <br/> Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) é Postado na janela que capturou esse ponteiro. <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Postado para fornecer uma atualização em um ponteiro que fez contato na área não cliente de uma janela ou quando um contato não capturado é movido sobre a área não cliente de uma janela. Enquanto o ponteiro estiver focalizando, a mensagem será direcionada a qualquer janela em que o ponteiro esteja. Enquanto o ponteiro está em contato com a superfície, o ponteiro é implicitamente capturado para a janela sobre a qual o ponteiro fez contato e essa janela continua a receber entrada para o ponteiro até que ele interrompa o contato. <br/> Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [<strong>WM_POINTERUPDATE</strong>] (WM-pointerupdate.MD) é Postado na janela que capturou esse ponteiro.<br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Enviado a uma janela quando ocorre uma ação significativa em uma janela descendente. Esta mensagem agora é estendida para incluir o evento [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD). Quando a janela filho está sendo criada, o sistema envia [<strong>WM_PARENTNOTIFY</strong>] (/Previous-Versions/Windows/Desktop/inputmsg/WM-parentnotify) logo antes da função [<strong>CreateWindow</strong>] (/Windows/Win32/API/WinUser/NF-WinUser-createwindowa) ou [<strong>CreateWindowEx</strong>] (/Windows/Win32/API/WinUser/NF-WinUser-createwindowexa) que cria a janela retorna. Quando a janela filho está sendo destruída, o sistema envia a mensagem antes que qualquer processamento para destruir a janela ocorra.<br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)). <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Enviado a uma janela inativa quando um ponteiro principal gera um [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) na janela. Desde que a mensagem permaneça sem tratamento, ela viaja para a cadeia de janelas pai até atingir a janela de nível superior. Os aplicativos podem responder a essa mensagem para especificar se desejam ser ativados.<br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)). <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Enviado para uma janela que está perdendo a captura de um ponteiro de entrada.<br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)).<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Enviado a uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ele. Esta mensagem contém informações sobre o dimensionamento do modo de exibição. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Enviado para uma janela quando um dispositivo de ponteiro é detectado dentro do intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Enviado a uma janela quando um dispositivo ponteiro tiver desem parte o intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Postado quando um ponteiro faz contato sobre a área do cliente de uma janela. Essa mensagem de entrada é direcionada para a janela sobre a qual o ponteiro faz contato, e o ponteiro é capturado implicitamente na janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato. <br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)).<br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Enviado a uma janela quando um novo ponteiro entra no intervalo de detecção na janela (focalizado) ou quando um ponteiro existente se move dentro dos limites da janela. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Enviado para uma janela quando um ponteiro deixa o intervalo de detecção sobre a janela (focalizar) ou quando um ponteiro se move para fora dos limites da janela. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Ocorre no processo que recebe a entrada quando a entrada do ponteiro é roteada para outro processo.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Enviado a todos os processos (configurados para encadeamento entre processos por meio de [<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e não manipulando atualmente a entrada do ponteiro), sempre associado a uma ID de ponteiro específica, quando uma mensagem [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) é recebida no processo atual. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Enviado quando entrada de ponteiro contínua, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para encadeamento de processo cruzado ([<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Postado quando um ponteiro que fez contato na área do cliente de uma janela quebra o contato. Essa mensagem de entrada é direcionada para a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber mensagens de entrada, incluindo a notificação [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) para o ponteiro até que ele interrompa o contato. <br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)). <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Postado para fornecer uma atualização em um ponteiro que fez contato na área do cliente de uma janela ou em um ponteiro não capturado em foco na área do cliente de uma janela. Enquanto o ponteiro estiver focalizando, a mensagem será direcionada a qualquer janela em que o ponteiro esteja. Enquanto o ponteiro está em contato com a superfície, o ponteiro é implicitamente capturado para a janela sobre a qual o ponteiro fez contato e essa janela continua a receber entrada para o ponteiro até que ele interrompa o contato. <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md)<br/></td>
<td>Postado na janela com o foco de teclado de primeiro plano quando uma roda de rolagem é girada. <br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)).<br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md)<br/></td>
<td>Postado na janela com o foco do teclado de primeiro plano quando uma roda de rolagem horizontal é girada. <br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = VS. 85)).<br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md)<br/></td>
<td>Enviado a uma janela em um toque para determinar o destino de toque mais provável. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de mensagem de entrada do ponteiro](wmpointer-reference.md)
</dt> </dl>

 

