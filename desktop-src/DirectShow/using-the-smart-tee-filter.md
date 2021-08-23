---
description: Usando o filtro Smart Tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Usando o filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8897a93e8be7582a4acce1a2822160c58cfe1df79eb2093bd5d96bad9629b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650767"
---
# <a name="using-the-smart-tee-filter"></a>Usando o filtro Smart Tee

Se um filtro de captura tiver pinos de captura e visualização separados, você poderá capturar de um durante a visualização do outro. Mas se o filtro não tiver nenhum pin de visualização, você poderá fazer a mesma coisa incluindo o filtro [Smart Tee](smart-tee-filter.md) no grafo. Esse filtro divide os dados do pino de captura em dois fluxos idênticos, um para captura e outro para visualização. O diagrama a seguir ilustra esse processo.

![grafo de captura com filtro smart tee](images/vidcap05.png)

O [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insere automaticamente o Filtro Smart Tee, se necessário. No entanto, se você usar métodos **IGraphBuilder** para criar seu grafo, e não **RenderStream,** talvez seja necessário inserir o filtro Smart Tee.

Antes de renderizar pins no filtro de captura, verifique se o filtro tem um pino de visualização ou um pino de porta de vídeo. Se isso não acontecer e você quiser visualizar, adicione o filtro Smart Tee ao grafo e conecte-o ao pino de captura no filtro de captura.

> [!Note]  
> Você pode tratar um pin de vp (porta de vídeo) como um tipo de pin de visualização, de modo que um filtro com um pin vp não precise de um filtro Smart Tee. No entanto, os pinos de VP têm alguns outros requisitos especiais. Para obter mais informações, consulte [Video Port Pins](video-port-pins.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Combinando captura e visualização de vídeo](combining-video-capture-and-preview.md)
</dt> <dt>

[Trabalhando com categorias de pino](working-with-pin-categories.md)
</dt> </dl>

 

 



