---
description: O objeto RealTimeStylus não coleta tinta inerentemente. Para usar o RealTimeStylus para coletar tinta, crie um plug-in do coletor de tinta.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection plug-ins do Ink-Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64966e2d088e9145fa4a0c0b29a7f7cc787b8435a3e4a609e75eae27b4e25524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967205"
---
# <a name="ink-collection-plug-ins"></a>Ink-Collection plug-ins do Ink-Collection

O [**objeto RealTimeStylus**](realtimestylus-class.md) não coleta tinta inerentemente. Para usar o **RealTimeStylus** para coletar tinta, crie um plug-in do coletor de tinta.

A seguir está um cenário mínimo para usar o [**objeto RealTimeStylus**](realtimestylus-class.md) em um formulário que coleta tinta.

1.  Crie um formulário que implemente a interface [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
2.  Crie um [**objeto RealTimeStylus**](realtimestylus-class.md) e anexe-o a um controle no formulário.
3.  De acordo com as notificações StylusDown, Packets e StylusUp na propriedade [Data Interest do](/previous-versions/ms574886(v=vs.100)) formulário.
4.  Nos métodos [**StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) do formulário, adicione código para manipular a caneta para baixo, pacotes e notificações de caneta que são enviadas do objeto [**RealTimeStylus**](realtimestylus-class.md) do formulário. Esse código deve armazenar os dados da caneta e criar e armazenar os traços.

Para ver um exemplo desse aplicativo, consulte o exemplo de amostra de coleção de tinta [RealTimeStylus.](realtimestylus-ink-collection-sample.md)

> [!Note]  
> Quando ocorrer um evento [DisplaySettingsChanged,](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) chame o método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) dos traços coletados em um manipulador de eventos DisplaySettingsChanged para recalcular as propriedades [Width](/previous-versions/ms582112(v=vs.100)) e [Height.](/previous-versions/ms582106(v=vs.100)) Isso é necessário para levar em conta possíveis alterações de dpi (pontos por polegada) resultantes do evento DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Coleta e reconhecedores de tinta

Nem a análise de tinta nem o reconhecimento de manuscrito são uma função do [**objeto RealTimeStylus.**](realtimestylus-class.md) Como o plug-in do coletor de tinta coleta tinta ou como você deseja reconhecer a tinta, você pode copiar a tinta para um objeto [RecognizerContext](/previous-versions/ms552546(v=vs.100)) ou [Divider.](/previous-versions/ms583616(v=vs.100)) Para obter mais informações sobre reconhecimento e análise de tinta, consulte [Sobre o reconhecimento de manuscrito](about-handwriting-recognition.md) ou o objeto [divisor](the-divider-object.md).

## <a name="static-rendering"></a>Renderização estática

Para renderizar tinta conforme ela está sendo coletada, anexe um objeto [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) ao [**objeto RealTimeStylus.**](realtimestylus-class.md) Para renderizar tinta depois que ela tiver sido coletada, use um [objeto Renderer](/previous-versions/ms552630(v=vs.100)) para desenhar os traços para o objeto [Gráfico apropriado.](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) Para obter mais informações sobre o objeto DynamicRenderer, consulte [Plug-ins de renderização dinâmica.](dynamic-renderer-plug-ins.md) Para ver um exemplo de renderização estática e dinâmica, consulte Amostra de coleção de tinta [realTimeStylus](realtimestylus-ink-collection-sample.md).

 

 
