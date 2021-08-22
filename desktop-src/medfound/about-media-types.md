---
description: Saiba mais sobre os tipos de mídia Microsoft Media Foundation. Um tipo de mídia descreve o formato de um fluxo de mídia.
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Sobre tipos de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3abce5d86b931a472dc07e1b6daf244f1456cfd3220f85c2b0e311f243a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975075"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Sobre tipos de mídia (Microsoft Media Foundation)

Um *tipo de mídia* descreve o formato de um fluxo de mídia. No Microsoft Media Foundation, os tipos de mídia são representados pela interface [**IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Essa interface herda a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Os detalhes de um tipo de mídia são especificados como atributos.

Para criar um novo tipo de mídia, chame a [**função MFCreateMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) Essa função retorna um ponteiro para a interface [**IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) O tipo de mídia inicialmente não tem atributos. Para definir os detalhes do formato, de definir os atributos relevantes.

Para ver uma lista de atributos de tipo de mídia, consulte [Atributos de tipo de mídia](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Principais tipos e subtipos

Duas informações importantes para qualquer tipo de mídia são o tipo principal e o subtipo.

-   O *tipo principal* é um GUID que define a categoria geral dos dados em um fluxo de mídia. Os principais tipos incluem vídeo e áudio. Para especificar o tipo principal, de definido o [atributo \_ MF MT \_ MAJOR \_ TYPE.](mf-mt-major-type-attribute.md) O [**método IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) retorna o valor desse atributo.
-   O *subtipo* define ainda mais o formato. Por exemplo, dentro do tipo principal de vídeo, há subtipos para RGB-24, RGB-32, YUY2 e assim por diante. No áudio, há áudio PCM, áudio de ponto flutuante IEEE e outros. O subtipo fornece mais informações do que o tipo principal, mas não define tudo sobre o formato. Por exemplo, subtipos de vídeo não definem o tamanho da imagem ou a taxa de quadros. Para especificar o subtipo, de definido o [atributo \_ MF MT \_ SUBTYPE.](mf-mt-subtype-attribute.md)

Todos os tipos de mídia devem ter um GUID de tipo principal e um GUID de subtipo. Para ver uma lista de GUIDs de tipo principal e subtipo, consulte [GUIDs de tipo de mídia.](media-type-guids.md)

## <a name="why-attributes"></a>Por que atributos?

Os atributos têm várias vantagens em relação às estruturas de formato que foram usadas em tecnologias anteriores, como DirectShow e o SDK Windows Formato de Mídia.

-   É mais fácil representar valores "não sei" ou "não se importa". Por exemplo, se você estiver escrevendo uma transformação de vídeo, talvez saiba com antecedência quais formatos RGB e YUV a transformação dá suporte, mas não às dimensões do quadro de vídeo, até que você as receba da fonte do vídeo. Da mesma forma, você pode não se importar com determinados detalhes, como os primários de vídeo. Com uma estrutura de formato, cada membro deve ser preenchido com *algum* valor. Como resultado, tornou-se comum usar zero para indicar um valor desconhecido ou padrão. Essa prática poderá causar erros se outro componente tratar zero como um valor legítimo. Com atributos, basta omitir os atributos desconhecidos ou não relevantes para o componente.

-   Conforme os requisitos mudaram ao longo do tempo, as estruturas de formato foram estendidas adicionando dados adicionais ao final da estrutura. Por exemplo, **WAVEFORMATEXTENSIBLE** estende a **estrutura WAVEFORMATEX.** Essa prática é propensa a erros, pois os componentes devem lançar ponteiros de estrutura para outros tipos de estrutura. Os atributos podem ser estendidos com segurança.
-   Estruturas de formato mutuamente incompatíveis foram definidas. Por exemplo, DirectShow define as estruturas **VIDEOINFOHEADER** **e VIDEOINFOHEADER2.** Os atributos são definidos independentemente uns dos outros, portanto, esse problema não surge.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 



