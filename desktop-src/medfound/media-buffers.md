---
description: Buffers de mídia
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Buffers de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105793739"
---
# <a name="media-buffers"></a>Buffers de mídia

Um buffer de mídia é um objeto COM que gerencia um bloco de memória, normalmente, para manter os dados de mídia. Os buffers de mídia são usados para mover dados de um componente de pipeline para o próximo. A maioria dos aplicativos não usa buffers de mídia diretamente, porque a sessão de mídia manipula todo o fluxo de dados entre objetos de pipeline. Você deve usar buffers de mídia se estiver escrevendo seu próprio componente de pipeline ou se estiver usando um componente de pipeline diretamente sem a sessão de mídia.

Os buffers de mídia expõem a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . Essa interface foi projetada para ler ou gravar qualquer tipo de dados. Quadros de vídeo descompactados exigem tratamento especial, pois podem ser armazenados em superfícies de Direct3D localizadas na memória de vídeo.

Esta seção contém os seguintes tópicos.



| Tópico                                                        | Descrição                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Trabalhando com buffers de mídia](working-with-media-buffers.md) | Descreve o comportamento geral dos buffers de mídia para todos os tipos de mídia. |
| [Buffers de vídeo descompactados](uncompressed-video-buffers.md) | Como trabalhar com buffers de mídia que contêm quadros de vídeo descompactados.  |
| [Buffer de superfície DirectX](directx-surface-buffer.md)         | Descreve como armazenar uma superfície do Direct3D em um buffer de mídia.         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de Media Foundation](media-foundation-primitives.md)
</dt> </dl>

 

 



