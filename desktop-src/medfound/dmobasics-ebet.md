---
description: DMO Básico
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: DMO Noções básicas (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24c7fb988d5e5225f292585a5562cce22e67c007175fa7ddc4cd86e40ec1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742355"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO Noções básicas (Microsoft Media Foundation)

Este tópico fornece uma breve visão geral dos DMOs que se relacionam com Windows Codecs de mídia. Para obter mais informações sobre DMOs, consulte [DirectX Media Objects](../directshow/directx-media-objects.md).

Um DMO é um objeto COM que transforma dados. Você passa dados para ele e eles retornam os dados transformados. No caso de um codificador codec DMO, você inseri dados de mídia descompactados e o DMO fornece dados de mídia compactados. A principal vantagem de usar DMOs é que todos eles implementam a mesma interface base, [**IMediaObject,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)que simplifica o trabalho com eles porque você pode usar o mesmo objeto, independentemente do tipo de transformação que está sendo executado.

Como há variáveis envolvidas em qualquer tipo de transformação de dados, a transformação áudio e vídeo deve levar em conta a ampla variedade de configurações de mídia possíveis. Os Windows codecs de Áudio e Vídeo de Mídia também suportam vários recursos especiais que você deve ser capaz de configurar usando o DMO.

Em geral, as informações de variável necessárias para os DMOs de codec compactar e descompactar mídia digital são transmitidas de uma das três maneiras:

-   De definir o tipo de entrada no DMO para transmitir as características da mídia descompactada que você passa para um codificador DMO e as características da mídia compactada que você passa para um decodificador DMO.
-   De definir o tipo de saída no DMO para transmitir as características da mídia compactada que são entregues por um codificador DMO e as características da mídia descompactada que são entregues por um DMO.
-   Usando os métodos da interface **IPropertyBag,** configure outras configurações que suportam os vários recursos dos DMOs codec como propriedades. **IPropertyBag** é uma interface COM padrão com suporte por todos os DMOs de codec.

Além disso, alguns recursos de codec são gerenciados usando outras interfaces específicas para os DMOs de codec. Essas interfaces são listadas para cada codec na seção [Objetos codec](codecobjects.md).

Os tipos de entrada e saída são específicos para fluxos de entrada e saída. Cada fluxo representa uma representação discreta do conteúdo. Por exemplo, o codificador Windows Media Video DMO tem um único fluxo de entrada e dois fluxos de saída. O fluxo de entrada aceita exemplos de vídeo descompactados. O primeiro dos dois fluxos de saída fornece amostras compactadas; o outro fornece exemplos descompactados. Os exemplos individuais em um fluxo de saída representam o mesmo conteúdo que os exemplos correspondentes no outro fluxo, mas cada fluxo entrega esses exemplos em um formato diferente.

Cada fluxo (entrada ou saída) dá suporte a um ou mais tipos de mídia. Um tipo de mídia, ou formato, é descrito por uma [**estrutura DMO \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Você pode consultar o DMO para os tipos que têm suporte em um fluxo de saída chamando [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Esse método retorna um tipo de saída válido (embora, em alguns casos, parcialmente incompleto) para esse fluxo. Você pode enumerar os tipos de mídia com suporte para um fluxo de saída fazendo chamadas repetidas para **GetOutputType**, incrementando o parâmetro de tipo a cada chamada. Quando o índice de tipo que você passa está fora dos limites, o método retorna **DMO E NO MORE \_ \_ \_ \_ ITEMS**. Os formatos de entrada podem ser enumerados da mesma maneira usando o [**método IMediaObject::GetInputType.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)

Os tipos enumerados pelo DMO são apenas os tipos "preferenciais", no entanto, outros tipos podem ter suporte. Você pode validar um tipo de saída chamando [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Use [**IMediaObject::SetInputType para**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) validar um tipo de entrada. Ambos os métodos retornarão **DMO E TYPE NOT \_ \_ \_ \_ ACCEPTED** se a estrutura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) passada for inválida. Alguns DMOs exigem que você de definir um tipo de saída antes de enumerar qualquer tipo de entrada. Os DMOs Windows codec de Áudio de Mídia e Vídeo têm entradas e saídas que têm validação interdependente. Ou seja, o tipo de saída definido definirá os critérios de validação para o tipo de entrada. Também há algumas propriedades que, quando definidas, alteram os tipos de entrada e saída válidos. Por esse motivo, você deve definir todas as propriedades desejadas no DMO antes de enumerar tipos.

Quando você tiver definido os tipos de saída e de entrada para o DMO, poderá começar a processar exemplos. Cada exemplo de entrada é passado para o codec usando uma chamada para [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)e cada exemplo de saída é entregue pelo codec quando você faz uma chamada para [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com DMOs codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
