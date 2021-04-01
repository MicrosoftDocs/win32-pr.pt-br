---
description: Interfaces de streaming do DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009977"
---
# <a name="directdraw-streaming-interfaces"></a>Interfaces de streaming do DirectDraw

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

Se você usar formatos de vídeo com suporte do DirectDraw em seus fluxos, as interfaces a seguir oferecem um controle mais poderoso sobre os dados do que as interfaces base mais genéricas.



| Interface                                                  | Descrição                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Define e recupera o formato de fluxo e o objeto DirectDraw associado ao fluxo de mídia; Essa interface deriva de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). Você também pode usar essa interface para criar amostras de vídeo. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Permite anexar amostras de vídeo a superfícies do DirectDraw; Essa interface deriva da interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Cada superfície anexada inclui um retângulo de recorte para facilitar a renderização. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de interfaces de streaming de multimídia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



