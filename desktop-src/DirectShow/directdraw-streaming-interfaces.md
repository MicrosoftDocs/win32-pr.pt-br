---
description: Interfaces de streaming do DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11e7eec0ec7ad82c0046b8c052ff00093b496c05495ec38590d201724d7620e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983046"
---
# <a name="directdraw-streaming-interfaces"></a>Interfaces de streaming do DirectDraw

> [!Note]  
> Essas APIs são preteridas. os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um DirectShow gráfico de filtro.

 

Se você usar formatos de vídeo com suporte do DirectDraw em seus fluxos, as interfaces a seguir oferecem um controle mais poderoso sobre os dados do que as interfaces base mais genéricas.



| Interface                                                  | Descrição                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Define e recupera o formato de fluxo e o objeto DirectDraw associado ao fluxo de mídia; Essa interface deriva de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). Você também pode usar essa interface para criar amostras de vídeo. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Permite anexar amostras de vídeo a superfícies do DirectDraw; Essa interface deriva da interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Cada superfície anexada inclui um retângulo de recorte para facilitar a renderização. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de interfaces de streaming de multimídia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



