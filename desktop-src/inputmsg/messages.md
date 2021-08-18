---
title: Mensagens
description: Os tópicos nesta seção fornecem as especificações de referência para notificações e mensagens de entrada de ponteiro específicas.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 076ba9d8b33bf2848d6088c4bac42b60ce9e19646abe5163358f25b063250b9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756948"
---
# <a name="messages"></a>Mensagens

Os tópicos nesta seção fornecem as especificações de referência para notificações e mensagens de entrada de ponteiro [específicas.](messages-and-notifications-portal.md)

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
<td>Enviado para uma janela, quando a entrada do ponteiro é detectada pela primeira vez, para determinar o destino de entrada mais provável para [Manipulação Direta.](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal) <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Postado quando um ponteiro faz contato sobre a área não cliente de uma janela. A mensagem tem como destino a janela sobre a qual o ponteiro faz contato. O ponteiro é implicitamente capturado para a janela para que a janela continue recebendo entrada para o ponteiro até que elebre o contato. <br/> Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) é postado na janela que capturou esse ponteiro. <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Postado quando um ponteiro que fez contato sobre a área não cliente de uma janela interrompe o contato. A mensagem tem como destino a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que elebre o contato, incluindo a notificação [<strong>WM_NCPOINTERUP</strong>](wm-ncpointerup.md). <br/> Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [<strong>WM_POINTERUP</strong>](wm-pointerup.md) é postado na janela que capturou esse ponteiro. <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Postado para fornecer uma atualização em um ponteiro que fez contato sobre a área não cliente de uma janela ou quando um contato sem controle de foco se move sobre a área não cliente de uma janela. Enquanto o ponteiro está passeando, a mensagem tem como alvo qualquer janela em que o ponteiro está acima. Enquanto o ponteiro está em contato com a superfície, o ponteiro é implicitamente capturado para a janela sobre a qual o ponteiro fez contato e essa janela continua recebendo entrada para o ponteiro até que ele interrompe o contato. <br/> Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada. Em vez disso, um [<strong>WM_POINTERUPDATE</strong>](wm-pointerupdate.md) é postado na janela que capturou esse ponteiro.<br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Enviado para uma janela quando ocorre uma ação significativa em uma janela descendente. Essa mensagem agora é estendida para incluir o evento [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md). Quando a janela filho está sendo criada, o sistema envia [<strong>WM_PARENTNOTIFY</strong>](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) logo antes da função [<strong>CreateWindow</strong>](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [<strong>CreateWindowEx</strong>](/windows/win32/api/winuser/nf-winuser-createwindowexa) que cria os retornos de janela. Quando a janela filho está sendo destruída, o sistema envia a mensagem antes de qualquer processamento para destruir a janela.<br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)). <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Enviado para uma janela inativa quando um ponteiro primário gera um [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) pela janela. Desde que a mensagem permaneça sem tratativas, ela percorre a cadeia de janelas pai até chegar à janela de nível superior. Os aplicativos podem responder a essa mensagem para especificar se desejam ser ativados.<br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)). <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Enviado para uma janela que está perdendo a captura de um ponteiro de entrada.<br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Enviado para uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ela. Esta mensagem contém informações sobre o dimensionamento do modo de exibição. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Enviado para uma janela quando um dispositivo de ponteiro é detectado dentro do intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Enviado para uma janela quando um dispositivo de ponteiro diminuiu o intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Postado quando um ponteiro faz contato sobre a área do cliente de uma janela. Essa mensagem de entrada tem como destino a janela sobre a qual o ponteiro faz contato e o ponteiro é implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que elebre o contato. <br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Enviado para uma janela quando um novo ponteiro entra no intervalo de detecção sobre a janela (passar o mouse) ou quando um ponteiro existente se move dentro dos limites da janela. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Enviado para uma janela quando um ponteiro deixa o intervalo de detecção sobre a janela (passar o mouse) ou quando um ponteiro se move para fora dos limites da janela. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Ocorre no processo que recebe entrada quando a entrada do ponteiro é roteada para outro processo.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Enviado para todos os processos (configurados para encadeamento entre processos por meio de [<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e não está tratando a entrada de ponteiro no momento) associado a uma ID de ponteiro específica, quando uma mensagem<strong>[ WM_POINTERUP</strong>](wm-pointerup.md) é recebida no processo atual. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Enviado quando a entrada do ponteiro em andamento, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para encadeamento entre processos ([<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Postado quando um ponteiro que fez contato sobre a área do cliente de uma janela interrompe o contato. Essa mensagem de entrada tem como destino a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber mensagens de entrada, incluindo a notificação [<strong>WM_POINTERUP</strong>](wm-pointerup.md) para o ponteiro até que elebre o contato. <br/> Uma janela recebe essa mensagem por meio de sua função [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)). <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Postado para fornecer uma atualização em um ponteiro que fez contato sobre a área do cliente de uma janela ou em um ponteiro semcaptura de foco sobre a área do cliente de uma janela. Enquanto o ponteiro está passeando, a mensagem tem como alvo qualquer janela em que o ponteiro está acima. Enquanto o ponteiro está em contato com a superfície, o ponteiro é implicitamente capturado para a janela sobre a qual o ponteiro fez contato e essa janela continua recebendo entrada para o ponteiro até que ele interrompe o contato. <br/>
<blockquote>
[!Important]<br />
Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))
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

 

