---
description: Um plug-in do reconhecedor é um objeto que monitora a movimentação da caneta do Tablet para gestos, manuscritos ou outros objetos.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Plug-ins do Recognizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3ac866a211a78e2d8f347e89ca20a1906f436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562594"
---
# <a name="recognizer-plug-ins"></a>Plug-ins do Recognizer

Um plug-in do reconhecedor é um objeto que monitora a movimentação da caneta do Tablet para gestos, manuscritos ou outros objetos.

## <a name="system-gestures"></a>Gestos do sistema

O objeto [**RealTimeStylus**](realtimestylus-class.md) reconhece gestos do sistema. O objeto **RealTimeStylus** adiciona um objeto [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) à fila [StylusQueues](/previous-versions/ms824786(v=msdn.10)) em resposta aos dados que terminam o gesto, como um objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para o [SystemGesture](/previous-versions/bb345349(v=vs.100)). Para obter mais informações, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>O objeto GestureRecognizer

O objeto [**GestureRecognizer**](gesturerecognizer-class.md) implementa as interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . O objeto **GestureRecognizer** reconhece os gestos do aplicativo. Internamente, o objeto **GestureRecognizer** usa o reconhecedor de gestos da Microsoft para executar o reconhecimento de gestos.

Quando o objeto [**GestureRecognizer**](gesturerecognizer-class.md) reconhece um gesto, ele adiciona dados da caneta personalizada à fila [StylusQueues](/previous-versions/ms824786(v=msdn.10)) em resposta ao objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para o traço. A propriedade [CustomDataId](/previous-versions/ms824748(v=msdn.10)) do objeto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) é definida como o valor [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) e a propriedade [Data](/previous-versions/ms824749(v=msdn.10)) do objeto CustomStylusData contém um objeto [GestureRecognitionData](/previous-versions/ms824594(v=msdn.10)) .

O diagrama a seguir ilustra como o objeto [**GestureRecognizer**](gesturerecognizer-class.md) adiciona dados aos dados da caneta eletrônica.

![ilustração de fluxo de dados GestureRecognizer](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

Neste diagrama, o círculo "SD" representa um objeto [StylusDownData](/previous-versions/ms824107(v=msdn.10)) e os círculos "P" representam os objetos [PacketsData](/previous-versions/ms824590(v=msdn.10)) que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronas. O círculo "SU" representa um objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e, em seguida, colocado na fila de saída. Os círculos "GR" representam os dados da caneta personalizada que são adicionados à fila de entrada pelo plug-in [**GestureRecognizer**](gesturerecognizer-class.md) em resposta à notificação da caneta associada a "su". Os dados da caneta personalizada "GR" são passados para os plug-ins síncronos e, em seguida, para a fila de saída antes de os próximos dados da caneta do Tablet serem processados. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

Por padrão, o objeto [**GestureRecognizer**](gesturerecognizer-class.md) reconhece apenas gestos de traço único; no entanto, o objeto **GestureRecognizer** pode ser definido para reconhecer gestos com vários traços. Para gestos com vários traços, o objeto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) é adicionado à fila [StylusQueues](/previous-versions/ms824786(v=msdn.10)) em resposta ao objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) para o traço final do gesto. Ao reconhecer gestos com vários traços, você pode receber notificações para sobreposição de conjuntos de traços. Por exemplo, o primeiro e o segundo traços juntos podem ser reconhecidos como um gesto e o segundo traço por si só pode ser reconhecido como um gesto. Para obter mais informações sobre o reconhecimento de gestos com vários traços, consulte a classe **GestureRecognizer** e a propriedade [MaxStrokeCount](/previous-versions/ms826053(v=msdn.10)) .

Se você estiver usando o objeto [**GestureRecognizer**](gesturerecognizer-class.md) para reconhecimento de gesto com vários traços, poderá obter um desempenho ideal usando um modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata e anexando o objeto **GestureRecognizer** ao objeto **RealTimeStylus** secundário. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Considerações especiais

A lista a seguir descreve outros pontos a serem levados em consideração ao usar o objeto [**GestureRecognizer**](gesturerecognizer-class.md) .

-   Você não deve anexar um objeto [**GestureRecognizer**](gesturerecognizer-class.md) a mais de um objeto [**RealTimeStylus**](realtimestylus-class.md) . Quando dois objetos **RealTimeStylus** aos quais o objeto **GestureRecognizer** está anexado são habilitados, ocorre o seguinte.
    -   O objeto [**GestureRecognizer**](gesturerecognizer-class.md) gera uma exceção em resposta à segunda chamada para seu método RealTimeStylusEnabled.
    -   O segundo objeto [**RealTimeStylus**](realtimestylus-class.md) que foi habilitado gera um objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) e notifica os plug-ins restantes em suas coleções de plug-in do erro.
    -   O objeto [**GestureRecognizer**](gesturerecognizer-class.md) para de reconhecer gestos.
-   O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção quando seu método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) é chamado com o parâmetro *GUID* definido como o GUID (identificador global exclusivo) [Microsoft. StylusInput. GestureRecognizer. GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) .
-   O objeto [**GestureRecognizer**](gesturerecognizer-class.md) é implementado como um wrapper Component Object Model (com) e você não pode chamar seus métodos de interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) diretamente. Para obter mais informações sobre a implementação COM e o objeto [**RealTimeStylus**](realtimestylus-class.md) , consulte [notas de implementação para as APIs StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-gesture-recognition"></a>Reconhecimento de gesto personalizado

Você pode criar um plug-in de reconhecedor personalizado que reconheça manuscritos, gestos ou outros objetos da:

-   Passando as informações de traço para um objeto [reconhecedor](/previous-versions/ms829434(v=msdn.10)) existente e usando o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) para adicionar os resultados ao fluxo de dados da caneta do Tablet.
-   Executar o reconhecimento no seu plug-in e usar o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) para adicionar os resultados ao fluxo de dados da caneta do Tablet.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gestos de aplicativo](application-gestures.md)
</dt> <dt>

[Gestos do sistema](system-gestures.md)
</dt> <dt>

[Linha do tempo de mensagens do mouse e eventos do sistema](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
