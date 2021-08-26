---
description: Eventos MSWebDVD
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Eventos MSWebDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a37eda7b8c2ebafc704d96195cc9e92e70fbd9d8bfda4aa7c971cd890e41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042706"
---
# <a name="mswebdvd-events"></a>Eventos MSWebDVD

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

> [!Note]  
> Essa API está preterida. Para obter informações sobre a reprodução e a navegação de DVD DirectShow, consulte [Aplicativos de DVD](dvd-applications.md).

 

O controle MSWebDVD Microsoft® ActiveX® notifica seu aplicativo quando ocorrem vários tipos de eventos internos ou quando determinadas informações são encontradas no disco.

A maioria dos eventos está relacionada a controles UOP (operação do usuário). Os autores de DVD podem codificar o disco para que qualquer comando de DVD (como **PlayForwards,** **Pause**, **ShowMenu** e assim por diante) possa ser desabilitado a qualquer momento. Por exemplo, a maioria dos discos não permitirá que os usuários avancem ou mostrem um menu enquanto o aviso DOLS está em reprodução. Depois que o aviso for final, o disco permitirá essas operações. Ao manipular os eventos UOP, seu aplicativo pode atualizar sua interface do usuário para mostrar ao usuário quais comandos atualmente são permitidos pelo disco. A maneira mais comum de fazer isso é desabilitando um botão. Por exemplo, se seu aplicativo recebeu um evento PlayForwards com **bEnabled** definido como **FALSE**, você poderá desabilitar o botão Reproduzir. Quando ele recebeu esse evento com **bEnabled definido** como **TRUE,** você pode habilitar o botão novamente.

Há três eventos que não estão relacionados a controles UOP. O **evento DVDNotify** notifica sua aplicação de muitos tipos diferentes de eventos relacionados a DVD, que são identificados no *parâmetro EventCode.* Alguns eventos têm informações adicionais nos *parâmetros Param1* e *Param2.* O **evento ReadyStateChange** notifica seu aplicativo de alterações na propriedade ReadyState MSWebDVD, que é uma propriedade comum a todos os ActiveX controles. O **evento UpdateOverlay** é enviado para aplicativos somente se eles estão hospedando MSWebDVD no modo sem janelas. Os aplicativos precisarão responder a esse evento somente se eles estão exibindo botões flutuantes sobre o retângulo de vídeo no modo de tela inteira.



| Evento                                                                  | Descrição                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Enviado quando o disco habilita ou desabilita a alteração do ângulo.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Enviado quando o disco habilita ou desabilita a alteração do fluxo de áudio.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Enviado quando **o comando ChangeCurrentSubpictureStream** foi habilitado ou desabilitado. |
| [**DVDNotify**](dvdnotify.md)                                         | Notifica um aplicativo de muitos eventos de DVD e instruções de disco diferentes.           |
| [**PauseOn**](pauseon.md)                                             | Enviado quando o **comando Pausar** tiver sido habilitado ou desabilitado.                         |
| [**PlayAtTime**](playattime.md)                                       | Enviado quando o **comando PlayAtTime** foi habilitado ou desabilitado.                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Enviado quando o **comando PlayAtTimeInTitle** foi habilitado ou desabilitado.             |
| [**PlayBackwards**](playbackwards.md)                                 | Enviado quando o **comando PlayBackwards** foi habilitado ou desabilitado.                 |
| [**PlayChapter**](playchapter.md)                                     | Enviado quando o **comando PlayChapter** foi habilitado ou desabilitado.                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Enviado quando o **comando PlayChapterInTitle** foi habilitado ou desabilitado.            |
| [**PlayForwards**](playforwards.md)                                   | Enviado quando o **comando PlayForwards** foi habilitado ou desabilitado.                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Enviado quando o **comando PlayNextChapter** foi habilitado ou desabilitado.               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Enviado quando o **comando PlayPrevChapter** foi habilitado ou desabilitado.               |
| [**PlayTitle**](playtitle.md)                                         | Enviado quando o **comando PlayTitle** foi habilitado ou desabilitado.                     |
| [**ReadyStateChange**](readystatechange.md)                           | Enviado quando a **propriedade ReadyState** do controle MSWebDVD foi alterada.            |
| [**ReplayChapter**](replaychapter.md)                                 | Enviado quando o **comando ReplayChapter** foi habilitado ou desabilitado.                 |
| [**Retomar**](resume.md)                                               | Enviado quando o **comando Retomar** tiver sido habilitado ou desabilitado.                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Enviado quando o **comando ReturnFromSubmenu** foi habilitado ou desabilitado.             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Enviado quando o disco habilita ou desabilita a seleção ou a ativação de botões de menu.   |
| [**ShowMenu**](showmenu.md)                                           | Enviado quando o disco habilita ou desabilita a exibição de um menu.                         |
| [**StillOff**](stilloff.md)                                           | Enviado quando o **comando StillOff** foi habilitado ou desabilitado.                      |
| [**Stop**](stop.md)                                                   | Enviado quando o **comando Parar** tiver sido habilitado ou desabilitado.                          |
| [**Updateoverlay**](updateoverlay.md)                                 | Enviado quando a superfície de sobreposição foi movida ou reescalada ou sua chave de cor foi alterada. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



