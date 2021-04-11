---
description: Noções básicas do DMO
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: Noções básicas do DMO (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b1aca2fcd7e70cf78e2e95135aee73c454b910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164189"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>Noções básicas do DMO (Microsoft Media Foundation)

Este tópico fornece uma breve visão geral do DMOs, pois eles se relacionam com os codecs do Windows Media. Para obter mais informações sobre DMOs, consulte [DirectX Media Objects](../directshow/directx-media-objects.md).

Um DMO é um objeto COM que transforma dados. Você passa dados para ele e retorna os dados transformados. No caso de um codec de codificador DMO, você insere dados de mídia descompactados e o DMO entrega dados de mídia compactados. A principal vantagem de usar o DMOs é que todos eles implementam a mesma interface base, [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), que simplifica o trabalho com eles porque você pode usar o mesmo objeto, independentemente do tipo de transformação que está sendo executada.

Como há variáveis envolvidas em qualquer tipo de transformação de dados, a transformação de áudio e vídeo deve levar em conta a ampla gama de possíveis configurações de mídia. Os codecs de áudio e vídeo do Windows Media também oferecem suporte a vários recursos especiais que você deve conseguir configurar usando o DMO.

Em geral, as informações de variáveis necessárias para o codec DMOs para compactar e descompactar mídia digital são transmitidas de uma das três maneiras:

-   Defina o tipo de entrada no DMO para transmitir as características da mídia descompactada que você passa para um codificador DMO e as características da mídia compactada que você passa para um decodificador DMO.
-   Defina o tipo de saída no DMO para transmitir as características da mídia compactada que são entregues por um codificador DMO e as características das mídias descompactadas que são entregues por um decodificador DMO.
-   Usando os métodos da interface **IPropertyBag** , defina outras configurações que dão suporte aos vários recursos do codec DMOs como propriedades. **IPropertyBag** é uma interface com padrão que é suportada por todos os DMOs do codec.

Além disso, alguns recursos de codec são gerenciados usando outras interfaces específicas para o codec DMOs. Essas interfaces são listadas para cada codec na seção [objetos de codec](codecobjects.md).

Os tipos de entrada e saída são específicos para fluxos de entrada e saída. Cada fluxo representa uma representação discreta do conteúdo. Por exemplo, o Windows Media Video Encoder DMO tem um único fluxo de entrada e dois fluxos de saída. O fluxo de entrada aceita exemplos de vídeo descompactados. O primeiro dos dois fluxos de saída fornece amostras compactadas; a outra fornece exemplos não compactados. Os exemplos individuais em um fluxo de saída representam o mesmo conteúdo que os exemplos correspondentes no outro fluxo, mas cada fluxo entrega esses exemplos em um formato diferente.

Cada fluxo (entrada ou saída) dá suporte a um ou mais tipos de mídia. Um tipo de mídia, ou formato, é descrito por uma estrutura de [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Você pode consultar o DMO para os tipos que têm suporte de um fluxo de saída chamando [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Esse método retorna um tipo de saída válido (embora em alguns casos parcialmente incompleto) para esse fluxo. Você pode enumerar os tipos de mídia com suporte para um fluxo de saída fazendo chamadas repetidas para **Getoutputtypetype**, incrementando o parâmetro de tipo com cada chamada. Quando o índice de tipo que você passa está fora dos limites, o método retorna **DMO \_ E \_ não \_ mais \_ itens**. Os formatos de entrada podem ser enumerados da mesma maneira usando o método [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) .

Os tipos enumerados pelo DMO são apenas os tipos "preferenciais", no entanto, outros tipos podem ter suporte. Você pode validar um tipo de saída chamando [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Use [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para validar um tipo de entrada. Os dois métodos retornarão o **\_ tipo DMO E \_ \_ não \_ aceito** se a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que você passou for inválida. Alguns DMOs exigem que você defina um tipo de saída antes de enumerar qualquer tipo de entrada. O codec de áudio e vídeo do Windows Media DMOs todos têm entradas e saídas que têm validação interdependentes. Ou seja, o tipo de saída definido definirá os critérios de validação para o tipo de entrada. Também há algumas propriedades que, quando definidas, alteram os tipos válidos de entrada e saída. Por esse motivo, você deve definir todas as propriedades desejadas no DMO antes de enumerar os tipos.

Quando você tiver definido os tipos de saída e entrada para o DMO, poderá começar a processar exemplos. Cada exemplo de entrada é passado para o codec usando uma chamada para [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput), e cada exemplo de saída é entregue pelo codec quando você faz uma chamada para [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
