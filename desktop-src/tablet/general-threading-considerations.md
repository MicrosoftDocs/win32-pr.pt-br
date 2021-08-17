---
description: Visão geral das considerações gerais de threading.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Considerações gerais sobre threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092570"
---
# <a name="general-threading-considerations"></a>Considerações gerais sobre threading

A seguir estão as considerações gerais de threading ao desenvolver para Tablet PC.

-   [Threads de aplicativo e não de aplicativo](#application-and-non-application-threads)
-   [Considerações sobre desempenho](#performance-considerations)
    -   [Manipuladores](#event-handlers)
    -   [Propriedade AutoRedraw](#autoredraw-property)
    -   [Propriedade DynamicRendering](#dynamicrendering-property)
-   [Considerações sobre threading de eventos](#event-threading-considerations)
    -   [Eventos de objetos InkCollector e InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [Eventos de coleção de objetos de tinta e traços](#ink-object-and-strokes-collection-events)
    -   [Eventos de reconhecimento](#recognition-events)
    -   [Eventos do Painel de Entrada de Caneta](#pen-input-panel-events)
-   [Tópicos relacionados](#related-topics)

## <a name="application-and-non-application-threads"></a>Threads de aplicativo e não de aplicativo

Todos os eventos de tinta são gerados em um thread de tinta de alta prioridade separado. Isso permite que a tinta flua sem problemas mesmo quando um aplicativo está sendo executado lentamente. No entanto, os manipuladores de eventos podem diminuir ou bloquear a renderização de tinta.

Todos os eventos de reconhecimento gerados por chamadas de método de reconhecimento em segundo plano são tratados em um thread de reconhecimento em segundo plano de prioridade normal separado.

Todos os eventos do mouse são gerados no thread principal da interface do usuário do aplicativo.

## <a name="performance-considerations"></a>Considerações sobre desempenho

### <a name="event-handlers"></a>Manipuladores de eventos

A API (interface de programação de aplicativo) da Plataforma de Tablet PC tem um modelo interativo para eventos em vez de um modelo de notificação. Mantenha o código em manipuladores de eventos curtos para reduzir o tempo em que a renderização de tinta é bloqueada. A coleção de tinta pelo tablet pc não está bloqueada, mas seu aplicativo não recebe a tinta enquanto seu aplicativo está bloqueado.

### <a name="autoredraw-property"></a>Propriedade AutoRedraw

Quando seu aplicativo estiver executando renderização personalizada ou quando seu aplicativo for sensível a problemas de pintura, você poderá lidar com a repintura por conta própria e definir a propriedade [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) como **false** para o objeto [**InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture.](inkpicture-control.md) Use os eventos na tabela a seguir para lidar com a reainting.



| Objeto ou controle                                            | Evento                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Objeto<br/> | Os eventos [Control.Invalidated e](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) [Control.Paint subjacentes.](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Objeto<br/>     | Os eventos [Control.Invalidated e](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) [Control.Paint subjacentes.](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)<br/>                                 |
| [InkPicture](inkpicture-control.md) Controle<br/>      | Eventos [Control.Invalidated e](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) [Control.Paint herdados do](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) controle [InkPicture.](inkpicture-control.md)<br/> |



 

### <a name="dynamicrendering-property"></a>Propriedade DynamicRendering

Quando seu aplicativo estiver executando a renderização personalizada ou quando você quiser as informações, mas não a tinta, você poderá lidar com a colocação de tinta por conta própria e desativar a renderização em tempo real de tinta definindo a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) como **false** para o objeto [**InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture.](inkpicture-control.md)

## <a name="event-threading-considerations"></a>Considerações sobre threading de eventos

Eventos da API da Plataforma de Tablet PC são gerados em vários threads.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Eventos de objetos InkCollector e InkOverlay

A [**maioria dos eventos de objeto InkCollector**](inkcollector-class.md) e [**InkOverlay**](inkoverlay-class.md) são gerados no thread de tinta. Somente os eventos do mouse para esses objetos são gerados no thread da interface do usuário. Por exemplo, para o objeto **InkCollector,** o evento [**MouseDown**](inkcollector-mousedown.md) é gerado no thread da interface do usuário e o [**evento CursorDown**](inkcollector-cursordown.md) é gerado no thread de tinta.

### <a name="ink-object-and-strokes-collection-events"></a>Eventos de coleção de objetos de tinta e traços

Os [**eventos de**](inkdisp-class.md) coleção de objetos Ink e [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) podem vir do thread de tinta ou do thread da interface do usuário. Quando seu aplicativo manipula o **objeto Ink** ou a coleção **Strokes,** o evento é gerado no thread da interface do usuário. Quando o [**objeto InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) atualiza o objeto **Ink** ou a coleção **Strokes,** o evento é gerado no thread de tinta.

Os [controles InkPicture](inkpicture-control-reference.md) e [InkEdit](inkedit-control-reference.md) operam em um STA (single-threaded apartment). Quando o controle InkPicture ou InkEdit atualiza o objeto [**Ink**](inkdisp-class.md) ou a coleção [**Strokes,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) o evento é gerado no thread da interface do usuário.

### <a name="recognition-events"></a>Eventos de reconhecimento

Os eventos de reconhecimento são gerados no thread da interface do usuário ou no thread de reconhecimento em segundo plano.

-   O método Recognize do [](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) controle [InkEdit](inkedit-control-reference.md) gera o evento [Recognition](/previous-versions/ms836436(v=msdn.10)) (somente Biblioteca Gerenciada) ou [**RecognitionResult**](inkedit-recognitionresult.md) (somente Automação) no thread da interface do usuário.
-   Os métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) e [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) adquira os eventos [**Recognition**](inkrecognizercontext-recognition.md) e [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) no thread de reconhecimento em segundo plano.

### <a name="pen-input-panel-events"></a>Eventos do Painel de Entrada de Caneta

[**Os eventos PenInputPanel**](peninputpanel-class.md) são gerados no thread no qual o **objeto PenInputPanel** é criado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft.Ink.InkCollector.DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft.Ink.InkCollector.AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

