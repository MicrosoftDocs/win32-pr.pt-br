---
description: Buffers de mídia
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Buffers de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef02570ab994f0a15a9b53f2df8a0ac0b96a91a3bf3f260c1bcc5f866ade87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827506"
---
# <a name="media-buffers"></a>Buffers de mídia

Um buffer de mídia é um objeto COM que gerencia um bloco de memória, normalmente para conter dados de mídia. Buffers de mídia são usados para mover dados de um componente de pipeline para o próximo. A maioria dos aplicativos não usa buffers de mídia diretamente, porque a Sessão de Mídia lida com todo o fluxo de dados entre objetos de pipeline. Você deverá usar buffers de mídia se estiver escrevendo seu próprio componente de pipeline ou se estiver usando um componente de pipeline diretamente sem a Sessão de Mídia.

Buffers de mídia expõem a interface [**IMFMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) Essa interface foi projetada para ler ou escrever qualquer tipo de dados. Quadros de vídeo descompactados exigem tratamento especial, pois podem ser armazenados em superfícies Direct3D localizadas na memória de vídeo.

Esta seção contém os seguintes tópicos.



| Tópico                                                        | Descrição                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Trabalhando com buffers de mídia](working-with-media-buffers.md) | Descreve o comportamento geral de buffers de mídia para todos os tipos de mídia. |
| [Buffers de vídeo descompactados](uncompressed-video-buffers.md) | Como trabalhar com buffers de mídia que contêm quadros de vídeo descompactados.  |
| [Buffer de superfície do DirectX](directx-surface-buffer.md)         | Descreve como armazenar uma superfície direct3D em um buffer de mídia.         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation primitivos](media-foundation-primitives.md)
</dt> </dl>

 

 



