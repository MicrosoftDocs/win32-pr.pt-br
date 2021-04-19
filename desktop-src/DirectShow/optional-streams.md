---
description: Fluxos opcionais
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Fluxos opcionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105767791"
---
# <a name="optional-streams"></a>Fluxos opcionais

Um DMO pode designar alguns de seus fluxos de saída como opcionais. Um fluxo opcional produz dados que o aplicativo pode descartar, seja completamente ou em exemplos ocasionais. Por exemplo, um fluxo opcional pode conter informações adicionais sobre um fluxo primário.

Para consultar se um fluxo é opcional, chame o método [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) e verifique o parâmetro *pdwFlags* . Os fluxos opcionais retornam \_ o \_ sinalizador de STREAMF de saída de DMO \_ ou \_ o \_ sinalizador opcional STREAMF de saída DMO \_ . Esses sinalizadores significam quase a mesma coisa; uma pequena diferença entre elas será explicada em breve.

Se um fluxo for opcional, o cliente poderá instruir o DMO a descartar dados desse fluxo quando ele processar a saída. Para fazer isso, chame o método [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) e defina o buffer de saída como **nulo** para cada fluxo que você deseja descartar. (O buffer de saída é especificado no membro **pBuffer** do buffer de dados de saída do [**DMO \_ \_ \_**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer).) Além disso, defina o \_ descarte de saída do processo DMO \_ \_ \_ quando \_ não houver nenhum \_ sinalizador de buffer no parâmetro *dwFlags* .

Para cada fluxo em que o ponteiro *pBuffer* é **nulo**, o DMO tentará descartar os dados. Se o fluxo for opcional, o DMO será garantido para descartar os dados. Se o fluxo não for opcional, o DMO descartará os dados quando possível, mas não será garantido. Se não for possível descartar os dados, ele definirá o \_ \_ \_ sinalizador incompleto de dados de saída do DMO BUFFERF \_ . Se você definir um ponteiro *pBuffer* como **nulo** , mas não definir a \_ saída do processo DMO \_ \_ descartar \_ quando \_ nenhum sinalizador de \_ buffer, o DMO não descartará os dados. Nesse caso, o DMO armazena em buffer a saída internamente ou simplesmente falha na chamada **ProcessOutput** .

A única diferença funcional entre o \_ sinalizador opcional de saída de DMO \_ STREAMF \_ e o sinalizador de saída de STREAMF do DMO \_ \_ \_ é o seguinte:

-   O \_ sinalizador opcional STREAMF de saída de DMO \_ \_ indica que o cliente não precisa definir um tipo de mídia nesse fluxo. No entanto, se o cliente começar a processar dados sem definir o tipo de mídia para esse fluxo, ele deverá descartar os dados desse fluxo para toda a duração do streaming. Se você quiser descartar amostras seletivamente, deverá definir o tipo de mídia.
-   O \_ \_ sinalizador incarded output STREAMF de saída de DMO \_ indica que, embora o fluxo seja opcional, ele sempre requer um tipo de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



