---
description: Este tópico descreve a diferença entre os tipos de mídia completa e os tipos de mídia parcial.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipos de mídia completos e parciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506351"
---
# <a name="complete-and-partial-media-types"></a>Tipos de mídia completos e parciais

Este tópico descreve a diferença entre os tipos de mídia completa e os tipos de mídia parcial.

## <a name="complete-media-types"></a>Tipos de mídia completos

Um tipo de mídia *completo* é aquele que define totalmente o formato do fluxo de mídia. Dado um tipo de mídia completo, um componente de pipeline pode analisar os dados de fluxo associados ao tipo de mídia, sem ambiguidade.

Para formatos descompactados, os tópicos a seguir definem os atributos necessários para um tipo de mídia completo:

-   Áudio: [tipos de mídia de áudio não compactados](uncompressed-audio-media-types.md)
-   Vídeo: [tipos de mídia de vídeo descompactados](uncompressed-video-media-types.md)

Para fluxos compactados (ou *codificados*), a definição de um tipo de mídia completo é definida pelo codec. No entanto, se algum atributo de tipo descompactado for conhecido para o fluxo compactado, esses valores deverão ser incluídos no tipo de mídia para o fluxo compactado. Por exemplo, se o tamanho do quadro for conhecido, defina o atributo de [**\_ tamanho do \_ quadro \_ MF MT**](mf-mt-frame-size-attribute.md) no tipo de mídia, embora tecnicamente um fluxo compactado não tenha um tamanho de quadro.

## <a name="partial-media-types"></a>Tipos de mídia parciais

Um tipo de mídia *parcial* não tem um ou mais dos atributos necessários para um tipo de mídia completo. Ao enumerar possíveis tipos de mídia, um componente Microsoft Media Foundation pode deixar um valor definido, para indicar que ele pode lidar com qualquer valor. Por exemplo, um processador de vídeo pode deixar a desdefinição do atributo de [**\_ taxa de \_ quadros \_ MF MT**](mf-mt-frame-rate-attribute.md) , para indicar que ele pode lidar com qualquer taxa de quadros e executará uma conversão de taxa de quadros, se necessário.

Se você criar um tipo de mídia parcial, ainda deverá incluir tantas informações quantas forem conhecidas. No entanto, um tipo de mídia não deve incluir informações incertas. É melhor que as informações estejam ausentes do que incorreto.

No mínimo, um tipo de mídia parcial deve incluir apenas dois atributos: [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) e [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md).

Às vezes Media Foundation componentes devem fornecer tipos de mídia completos:

-   As fontes de mídia devem fornecer tipos de saída completos.
-   Os decodificadores devem fornecer tipos de saída completos, depois que o tipo de entrada é definido. Antes que o tipo de entrada seja definido, um decodificador pode fornecer um tipo de saída parcial.
-   Os codificadores devem fornecer tipos de entrada completos, depois que o tipo de saída for definido. Antes de o tipo de saída ser definido, um codificador pode fornecer um tipo de entrada parcial.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 



