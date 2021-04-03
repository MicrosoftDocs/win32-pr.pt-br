---
description: Criando objetos de fluxo de multimídia e amostras de fluxo
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: Criando objetos de fluxo de multimídia e amostras de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930158"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>Criando objetos de fluxo de multimídia e amostras de fluxo

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

Os objetos que dão suporte à interface [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) são os contêineres básicos para fluxos de dados de multimídia. A interface **IMultiMediaStream** inclui métodos que enumeram os fluxos de dados do objeto; Normalmente, esses fluxos são dados de vídeo e áudio, mas podem incluir dados de qualquer formato, como legendas codificadas, texto sem formatação ou código de informa de SMPTE. No entanto, a interface **IMultiMediaStream** é um contêiner genérico; os desenvolvedores podem criar outras versões da interface que dão suporte a formatos de dados específicos. Os objetos que implementam a interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , por exemplo, podem enumerar e controlar fluxos de qualquer formato de dados do DirectShow. Como os fluxos de dados individuais são de formato específico, eles dão suporte a pelo menos duas interfaces diferentes: uma genérica e uma específica de dados. Cada fluxo dá suporte à interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) , que fornece métodos para recuperar seu formato e um ponteiro para o fluxo em si. A interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) , por outro lado, tem métodos que lidam especificamente com a renderização de dados de vídeo. Qualquer interface derivada de **IMultiMediaStream** também dá suporte à criação de amostras de fluxo, as unidades básicas de transmissão de dados.

Um exemplo de multimídia é uma referência a um objeto que contém os dados de mídia. Para uma imagem de vídeo, essa é uma superfície do DirectDraw. O conteúdo exato do exemplo varia, dependendo do tipo de mídia (som, texto e assim por diante). Como um exemplo é apenas uma referência ao objeto de dados, qualquer número de amostras de fluxo pode se referir ao mesmo objeto. A interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) fornece métodos que obtêm e definem as características de uma amostra, como a hora de início e de término, o status e a associação de fluxo. O método [**IStreamSample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) atualiza os dados do exemplo no caso de fluxos legíveis. Para fluxos graváveis, ele gravará os dados do exemplo no fluxo. Normalmente, você usa o método **Update** em um loop que processa, transfere ou armazena dados de streaming.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a arquitetura de streaming de multimídia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



