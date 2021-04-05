---
description: O objeto RealTimeStylus não coleta a tinta de forma inerente. Para usar o RealTimeStylus para coletar tinta, crie um plug-in de coletor de tinta.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Plug-ins Ink-Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826879"
---
# <a name="ink-collection-plug-ins"></a>Plug-ins Ink-Collection

O objeto [**RealTimeStylus**](realtimestylus-class.md) não coleta a tinta de forma inerente. Para usar o **RealTimeStylus** para coletar tinta, crie um plug-in de coletor de tinta.

Veja a seguir um cenário mínimo para usar o objeto [**RealTimeStylus**](realtimestylus-class.md) em um formulário que coleta tinta.

1.  Crie um formulário que implemente a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Crie um objeto [**RealTimeStylus**](realtimestylus-class.md) e anexe-o a um controle no formulário.
3.  Defina interesse nas notificações StylusDown, pacotes e StylusUp na propriedade [DataInterest](/previous-versions/ms574886(v=vs.100)) do formulário.
4.  Nos métodos [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) do formulário, adicione o código para lidar com as notificações de caneta para baixo, pacotes e canetas que são enviadas do objeto [**RealTimeStylus**](realtimestylus-class.md) do formulário. Esse código deve armazenar os dados da caneta e criar e armazenar os traços.

Para obter uma amostra desse aplicativo, consulte exemplo de amostra de [coleção de tinta do RealTimeStylus](realtimestylus-ink-collection-sample.md) .

> [!Note]  
> Quando ocorre um evento [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) , chame o método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) dos traços coletados em um manipulador de eventos DisplaySettingsChanged para recalcular as propriedades [Width](/previous-versions/ms582112(v=vs.100)) e [Height](/previous-versions/ms582106(v=vs.100)) . Isso é necessário para levar em conta as alterações de DPI (pontos por polegada) possíveis que resultam do evento DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Coleta e reconhecedores de tinta

Nenhuma análise de tinta nem reconhecimento de manuscrito é uma função do objeto [**RealTimeStylus**](realtimestylus-class.md) . Como o plug-in do coletor de tinta coleta tinta ou como você deseja reconhecer a tinta, você pode copiar a tinta para um objeto [RecognizerContext](/previous-versions/ms552546(v=vs.100)) ou [divisória](/previous-versions/ms583616(v=vs.100)) . Para obter mais informações sobre reconhecimento e análise de tinta, consulte [sobre o reconhecimento de manuscrito](about-handwriting-recognition.md) ou [o objeto divisória](the-divider-object.md).

## <a name="static-rendering"></a>Renderização estática

Para renderizar a tinta à medida que ela está sendo coletada, anexe um objeto [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) ao objeto [**RealTimeStylus**](realtimestylus-class.md) . Para renderizar a tinta após ela ter sido coletada, use um objeto de [processador](/previous-versions/ms552630(v=vs.100)) para desenhar os traços para o objeto [gráfico](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) apropriado. Para obter mais informações sobre o objeto DynamicRenderer, consulte [plug-ins de processamento dinâmico](dynamic-renderer-plug-ins.md). Para obter um exemplo de renderização estática e dinâmica, consulte [exemplo de coleta de tinta do RealTimeStylus](realtimestylus-ink-collection-sample.md).

 

 
