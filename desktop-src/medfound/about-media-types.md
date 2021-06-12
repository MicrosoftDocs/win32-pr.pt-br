---
description: Saiba mais sobre os tipos de mídia no Microsoft Media Foundation. Um tipo de mídia descreve o formato de um fluxo de mídia.
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Sobre os tipos de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263c2b473e378e6ae5dc75453b20d02dce61818f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010899"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Sobre os tipos de mídia (Microsoft Media Foundation)

Um *tipo de mídia* descreve o formato de um fluxo de mídia. No Microsoft Media Foundation, os tipos de mídia são representados pela interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Essa interface herda a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Os detalhes de um tipo de mídia são especificados como atributos.

Para criar um novo tipo de mídia, chame a função [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) . Essa função retorna um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . O tipo de mídia inicialmente não tem nenhum atributo. Para definir os detalhes do formato, defina os atributos relevantes.

Para obter uma lista de atributos de tipo de mídia, consulte [atributos de tipo de mídia](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Tipos e subtipos principais

Duas partes importantes de informações para qualquer tipo de mídia são o tipo principal e o subtipo.

-   O *tipo principal* é um GUID que define a categoria geral dos dados em um fluxo de mídia. Os tipos principais incluem vídeo e áudio. Para especificar o tipo principal, defina o atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) . O método [**IMFMediaType:: Getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) retorna o valor desse atributo.
-   O *subtipo* define ainda mais o formato. Por exemplo, dentro do tipo principal de vídeo, há subtipos para RGB-24, RGB-32, YUY2 e assim por diante. No áudio, há áudio PCM, áudio de ponto flutuante IEEE e outros. O subtipo fornece mais informações do que o tipo principal, mas não define tudo sobre o formato. Por exemplo, os subtipos de vídeo não definem o tamanho da imagem ou a taxa de quadros. Para especificar o subtipo, defina o atributo de [ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md) .

Todos os tipos de mídia devem ter um GUID de tipo principal e um GUID de subtipo. Para obter uma lista de principais tipos e GUIDs de subtipo, consulte [GUIDs de tipo de mídia](media-type-guids.md).

## <a name="why-attributes"></a>Por que atributos?

Os atributos têm várias vantagens sobre as estruturas de formato que foram usadas em tecnologias anteriores, como o DirectShow e o Windows Media Format SDK.

-   É mais fácil representar valores "não sei" ou "não se preocupe". Por exemplo, se você estiver escrevendo uma transformação de vídeo, talvez saiba com antecedência quais formatos RGB e YUV dão suporte à transformação, mas não as dimensões do quadro de vídeo, até que você os obtenha da fonte de vídeo. Da mesma forma, talvez você não se preocupa com determinados detalhes, como os primários de vídeo. Com uma estrutura de formato, todos os membros devem ser preenchidos com *algum* valor. Como resultado, tornou-se comum usar zero para indicar um valor desconhecido ou padrão. Essa prática poderá causar erros se outro componente tratar zero como um valor legítimo. Com atributos, você simplesmente omite os atributos que são desconhecidos ou não são relevantes para seu componente.

-   À medida que os requisitos tiverem mudado ao longo do tempo, as estruturas de formato foram estendidas adicionando dados adicionais ao final da estrutura. Por exemplo, **WAVEFORMATEXTENSIBLE** estende a estrutura **WAVEFORMATEX** . Essa prática está sujeita a erros, porque os componentes devem converter ponteiros de estrutura para outros tipos de estrutura. Os atributos podem ser estendidos com segurança.
-   Estruturas de formato incompatíveis mutuamente foram definidas. Por exemplo, o DirectShow define as estruturas **VIDEOINFOHEADER** e **VIDEOINFOHEADER2** . Os atributos são definidos de forma independente um do outro, portanto, esse problema não ocorre.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 



