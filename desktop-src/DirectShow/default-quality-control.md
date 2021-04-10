---
description: Controle de qualidade padrão
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Controle de qualidade padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009885"
---
# <a name="default-quality-control"></a>Controle de qualidade padrão

As [classes base do DirectShow](directshow-base-classes.md) implementam alguns comportamentos padrão para o controle de qualidade de vídeo.

As mensagens de qualidade começam no renderizador. A classe base para renderizadores de vídeo é [**CBaseVideoRenderer**](cbasevideorenderer.md), que tem o seguinte comportamento:

1.  Quando o renderizador de vídeo recebe um exemplo, ele compara o carimbo de data/hora no exemplo com o tempo de referência atual.
2.  O processador de vídeo gera uma mensagem de qualidade. Na classe base, o membro de **proporção** da mensagem de qualidade é limitado a um intervalo de 500 (50%) a 2000 (200%). Os valores fora desse intervalo podem resultar em alterações de qualidade abrupta.
3.  Por padrão, o processador de vídeo envia a mensagem de qualidade para o pino de saída upstream (o PIN conectado ao seu PIN de entrada). Os aplicativos podem substituir esse comportamento chamando o método **SetSink** .

O que acontece em seguida depende do filtro upstream. Normalmente, esse é um filtro de transformação. A classe base para filtros de transformação é [**CTransformFilter**](ctransformfilter.md), que usa as classes [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) para implementar Pins de entrada e saída. Juntas, essas classes têm o seguinte comportamento:

1.  O método [**CTransformOutputPin:: Notify**](ctransformoutputpin-notify.md) chama [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md), um método particular na classe base de filtro.
2.  Os filtros derivados podem substituir **AlterQuality** para manipular a mensagem de qualidade. Por padrão, o **AlterQuality** ignora a mensagem de qualidade.
3.  Se **AlterQuality** não tratar a mensagem de qualidade, o pino de saída chamará [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md), um método particular no PIN de entrada do filtro.
4.  **PassNotify** passa a mensagem de qualidade para o local apropriado — o próximo pino de saída upstream ou um Gerenciador de qualidade personalizado.

Supondo que nenhum filtro de transformação manipule a mensagem de qualidade, a mensagem eventualmente atinge o pino de saída no filtro de origem. Nas classes base, [**CBasePin:: Notify**](cbasepin-notify.md) retorna E \_ NOTIMPL. Como um filtro de origem específico manipula as mensagens de qualidade depende da natureza da origem. Algumas fontes, como a captura de vídeo ao vivo, não podem executar um controle de qualidade significativo. Outras fontes podem ajustar a taxa na qual elas fornecem exemplos.

O diagrama a seguir ilustra o comportamento padrão.

![controle de qualidade nas classes base](images/quality-control.png)

O processador de vídeo base implementa **IQualityControl:: Notify**, o que significa que você pode passar mensagens de qualidade para o próprio processador. Se você definir o membro de **proporção** como um valor menor que 1000, o processador de vídeo inserirá um período de espera entre cada quadro que ele renderiza, na lentidão do processador. (Você pode fazer isso para reduzir o uso do sistema, por exemplo.) Para obter mais informações, consulte [**CBaseVideoRenderer:: ThrottleWait**](cbasevideorenderer-throttlewait.md). Definir o membro de **proporção** como um valor maior que 1000 não tem efeito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de controle de qualidade](quality-control-management.md)
</dt> </dl>

 

 



