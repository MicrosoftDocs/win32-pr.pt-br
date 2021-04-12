---
description: Tipos de mídia
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Tipos de mídia (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297973"
---
# <a name="media-types-media-foundation"></a>Tipos de mídia (Media Foundation)

Um *tipo de mídia* é uma maneira de descrever o formato de um fluxo de mídia. No Media Foundation, os tipos de mídia são representados pela interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Os aplicativos usam tipos de mídia para descobrir o formato de um arquivo de mídia ou fluxo de mídia. Os objetos no pipeline de Media Foundation usam tipos de mídia para negociar os formatos que serão entregues ou recebidos.

Esta seção contém os seguintes tópicos.



| Tópico                                                                    | Descrição                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Sobre os tipos de mídia](about-media-types.md)                               | Visão geral dos tipos de mídia no Media Foundation.                             |
| [GUIDs de tipo de mídia](media-type-guids.md)                                 | Lista os GUIDs definidos para tipos e subtipos principais.                            |
| [Tipos de mídia de áudio](audio-media-types.md)                               | Como criar tipos de mídia para formatos de áudio.                                     |
| [Tipos de mídia de vídeo](video-media-types.md)                               | Como criar tipos de mídia para formatos de vídeo.                                     |
| [Tipos de mídia completos e parciais](complete-and-partial-media-types.md) | Descreve a diferença entre os tipos de mídia completa e os tipos de mídia parcial.   |
| [Conversões de tipo de mídia](media-type-conversions.md)                     | Como converter entre Media Foundation tipos de mídia e estruturas de formato mais antigas. |
| [Funções auxiliares de tipo de mídia](media-type-helper-functions.md)           | Uma lista de funções que manipulam ou obtêm informações de um tipo de mídia.        |
| [Código de depuração do tipo de mídia](media-type-debugging-code.md)               | Código de exemplo que mostra como exibir um tipo de mídia durante a depuração.                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de Media Foundation](media-foundation-primitives.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 



