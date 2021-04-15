---
description: Visão geral das considerações gerais de Threading.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Considerações gerais sobre Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f825ec7a1397dae7d60aa14b31603ee76a2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501833"
---
# <a name="general-threading-considerations"></a>Considerações gerais sobre Threading

A seguir estão as considerações gerais de Threading ao desenvolver para o Tablet PC.

-   [Aplicativos e threads que não são de aplicativo](#application-and-non-application-threads)
-   [Considerações sobre desempenho](#performance-considerations)
    -   [Manipuladores de eventos](#event-handlers)
    -   [Propriedade de redesenhot](#autoredraw-property)
    -   [Propriedade DynamicRendering](#dynamicrendering-property)
-   [Considerações sobre Threading de eventos](#event-threading-considerations)
    -   [Eventos de objetos InkCollector e InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [Eventos de coleção de traços e objetos de tinta](#ink-object-and-strokes-collection-events)
    -   [Eventos de reconhecimento](#recognition-events)
    -   [Eventos do painel de entrada da caneta](#pen-input-panel-events)
-   [Tópicos relacionados](#related-topics)

## <a name="application-and-non-application-threads"></a>Aplicativos e threads que não são de aplicativo

Todos os eventos de tinta são gerados em um thread de tinta separado e de alta prioridade. Isso permite que a tinta flua suavemente mesmo quando um aplicativo está em execução lenta. No entanto, os manipuladores de eventos podem diminuir ou bloquear a renderização da tinta.

Todos os eventos de reconhecimento gerados pelas chamadas de método de reconhecimento em segundo plano são tratados em um thread de reconhecimento em segundo plano de prioridade normal separado.

Todos os eventos de mouse são gerados no thread da interface do usuário principal do aplicativo.

## <a name="performance-considerations"></a>Considerações sobre desempenho

### <a name="event-handlers"></a>Manipuladores de eventos

A API (interface de programação de aplicativo) da plataforma do Tablet PC tem um modelo interativo para eventos em vez de um modelo de notificação. Mantenha o código nos manipuladores de eventos curtos para reduzir o tempo que a renderização de tinta é bloqueada. A coleção de tinta pelo Tablet PC não é bloqueada, mas seu aplicativo não recebe a tinta enquanto seu aplicativo está bloqueado.

### <a name="autoredraw-property"></a>Propriedade de redesenhot

Quando seu aplicativo estiver executando renderização personalizada ou quando seu aplicativo for sensível a problemas de pintura, você poderá lidar com a repintura por conta própria e definir a propriedade [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) como **false** para o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control.md) . Use os eventos na tabela a seguir para lidar com a repintura.



| Objeto ou controle                                            | Evento                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Objeto<br/> | Os eventos Control. [Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) do controle subjacente.<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Objeto<br/>     | Os eventos Control. [Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) do controle subjacente.<br/>                                 |
| [InkPicture](inkpicture-control.md) Controlo<br/>      | Controle herdado do controle [InkPicture](inkpicture-control.md) [. eventos invalidados](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/> |



 

### <a name="dynamicrendering-property"></a>Propriedade DynamicRendering

Quando seu aplicativo estiver executando renderização personalizada ou quando você quiser as informações, mas não a tinta, você poderá lidar com a tinta por conta própria e desativar a renderização em tempo real da tinta definindo a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) como **false** para o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control.md) .

## <a name="event-threading-considerations"></a>Considerações sobre Threading de eventos

Os eventos da API da plataforma do Tablet PC são gerados em vários threads.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Eventos de objetos InkCollector e InkOverlay

A maioria dos eventos de objeto [**InkCollector**](inkcollector-class.md) e [**InkOverlay**](inkoverlay-class.md) são gerados no thread de tinta. Somente os eventos do mouse para esses objetos são gerados no thread da interface do usuário. Por exemplo, para o objeto **InkCollector** , o evento [**MouseDown**](inkcollector-mousedown.md) é gerado no thread da interface do usuário e o evento [**CursorDown**](inkcollector-cursordown.md) é gerado no thread de tinta.

### <a name="ink-object-and-strokes-collection-events"></a>Eventos de coleção de traços e objetos de tinta

Os eventos de coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e objetos de [**tinta**](inkdisp-class.md) podem vir do thread de tinta ou do thread de interface do usuário. Quando o aplicativo manipula o objeto de **tinta** ou a coleção de **traços** , o evento é gerado no thread da interface do usuário. Quando o [**InkCollector**](inkcollector-class.md) ou o objeto [**InkOverlay**](inkoverlay-class.md) atualiza o objeto de **tinta** ou a coleção de **traços** , o evento é gerado no thread de tinta.

Os controles [InkPicture](inkpicture-control-reference.md) e [InkEdit](inkedit-control-reference.md) operam em um STA (single-threaded apartment). Quando o controle InkPicture ou InkEdit atualiza o objeto de [**tinta**](inkdisp-class.md) ou a coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , o evento é gerado no thread da interface do usuário.

### <a name="recognition-events"></a>Eventos de reconhecimento

Os eventos de reconhecimento são gerados no thread da interface do usuário ou no thread de reconhecimento em segundo plano.

-   O método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) do controle [InkEdit](inkedit-control-reference.md) gera o evento de [reconhecimento](/previous-versions/ms836436(v=msdn.10)) (somente biblioteca gerenciada) ou [**RecognitionResult**](inkedit-recognitionresult.md) (somente automação) no thread da interface do usuário.
-   Os métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) e [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) geram os eventos de [**reconhecimento**](inkrecognizercontext-recognition.md) e [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) no thread de reconhecimento em segundo plano.

### <a name="pen-input-panel-events"></a>Eventos do painel de entrada da caneta

Os eventos [**PenInputPanel**](peninputpanel-class.md) são gerados no thread em que o objeto **PenInputPanel** é criado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink. InkCollector. DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft. Ink. InkCollector. AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

