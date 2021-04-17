---
description: Usando o filtro de "t inteligente"
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Usando o filtro de "t inteligente"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780550"
---
# <a name="using-the-smart-tee-filter"></a>Usando o filtro de "t inteligente"

Se um filtro de captura tiver Pins de captura e de visualização separados, você poderá capturar de um durante a visualização do outro. Mas se o filtro não tiver nenhum pino de visualização, você poderá fazer a mesma coisa, incluindo o filtro de " [t" inteligente](smart-tee-filter.md) no grafo. Esse filtro divide os dados do pino de captura em dois fluxos idênticos, um para captura e outro para visualização. O diagrama a seguir ilustra esse processo.

![capturar grafo com o filtro de "inteligente"](images/vidcap05.png)

O método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insere automaticamente o filtro de "t inteligente", se necessário. No entanto, se você usar métodos **IGraphBuilder** para criar seu grafo, e não **RenderStream**, talvez seja necessário inserir o filtro de "t inteligente".

Antes de renderizar Pins no filtro de captura, verifique se o filtro tem um PIN de visualização ou um PIN de porta de vídeo. Se não tiver, e você quiser Visualizar, adicione o filtro de "t Smart" ao grafo e conecte-o ao PIN de captura no filtro de captura.

> [!Note]  
> Você pode tratar um PIN de porta de vídeo (VP) como um tipo de pino de visualização, de modo que um filtro com um VP PIN não precisa de um filtro de monitoração inteligente. No entanto, o VP de Pins tem alguns outros requisitos especiais. Para obter mais informações, consulte [pinos de porta de vídeo](video-port-pins.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Combinando captura de vídeo e visualização](combining-video-capture-and-preview.md)
</dt> <dt>

[Trabalhando com categorias de PIN](working-with-pin-categories.md)
</dt> </dl>

 

 



