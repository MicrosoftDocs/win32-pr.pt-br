---
description: As seguintes considerações de Threading do Tablet PC são específicas para quando Component Object Model (COM) e a automação são usadas.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Considerações de Threading COM e de automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796245"
---
# <a name="com-and-automation-threading-considerations"></a>Considerações de Threading COM e de automação

As seguintes considerações de Threading do Tablet PC são específicas para quando Component Object Model (COM) e a automação são usadas.

-   [Acesso thread-safe](#thread-safety)
-   [Aplicativos STA e MTA](#sta-and-mta-applications)
-   [InkCollector e InkOverlay](#inkcollector-and-inkoverlay)
-   [Coletores de eventos](#event-sinks)
-   [Exceções nos manipuladores de eventos](#exceptions-within-event-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="thread-safety"></a>Acesso thread-safe

Exceto pelos controles [InkPicture](inkpicture-control.md) e [InkEdit](inkedit-control.md) , os objetos do Tablet PC são thread-safe e são marcados como ambos. Ao ser marcado como ambos, eles podem ser executados em um STA (single-threaded apartment) ou em um MTA (multithreaded apartment).

O Windows Forms usa o modelo STA porque o Windows Forms se baseia em janelas nativas do Win32 que são inerentemente segmentadas em apartamento.

## <a name="sta-and-mta-applications"></a>Aplicativos STA e MTA

Se seu aplicativo for executado em um MTA ou usar o FTM (marshaled Threading) gratuito, você deverá escrever código de thread-safe; no entanto, ao fazer isso, você pode melhorar certos problemas de desempenho de manipulação de eventos.

## <a name="inkcollector-and-inkoverlay"></a>InkCollector e InkOverlay

Seu aplicativo não deve liberar sua referência final para o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) , destruindo, assim, o objeto diretamente do thread de tinta. Em vez disso, o aplicativo deve liberar o **InkCollector** ou o objeto **InkOverlay** de um thread de aplicativo.

**Cuidado:** Um aplicativo que está marcado como MTA ou usa o FTM, que permite chamadas diretas do thread de tinta para o apartamento do aplicativo, pode liberar sua referência final para o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) diretamente do thread de tinta; no entanto, isso causa falha de aplicativo irrecuperável.

## <a name="event-sinks"></a>Coletores de eventos

Se seu aplicativo não estiver usando o FTM e um objeto e seu coletor de eventos forem criados em diferentes Apartments, o evento será executado no thread que está atendendo ao coletor de eventos.

## <a name="exceptions-within-event-handlers"></a>Exceções nos manipuladores de eventos

As exceções geradas de dentro de manipuladores de eventos do Tablet PC são consumidas e não são visíveis para o restante ou seu aplicativo. Da mesma forma, os valores HRESULT não são propagados de manipuladores de eventos do Tablet PC. Se um aplicativo que usa a camada COM gera uma exceção, o thread em segundo plano é encerrado e a exceção será perdida. Nenhum manipulador de eventos adicional será chamado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de coletores de eventos do C++](c---event-sinks-sample.md)
</dt> <dt>

[Considerações gerais sobre Threading](general-threading-considerations.md)
</dt> <dt>

[Considerações sobre Threading de biblioteca gerenciada](managed-library-threading-considerations.md)
</dt> </dl>

 

 



