---
description: Configurações Fluxos
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Configurações Fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7c30f783a8c13b00020c2dac62cd11e2a79d6f2ea66af01f715c3cb389853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830965"
---
# <a name="optional-streams"></a>Configurações Fluxos

Um DMO pode designar alguns de seus fluxos de saída como opcionais. Um fluxo opcional produz dados que o aplicativo pode descartar, seja por completo ou por exemplos ocasionais. Por exemplo, um fluxo opcional pode conter informações adicionais sobre um fluxo primário.

Para consultar se um fluxo é opcional, chame o método [**IMediaObject::GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) e verifique o *parâmetro pdwFlags.* Os fluxos opcionais retornam o sinalizador DMO OUTPUT STREAMF DISCARDABLE ou o sinalizador \_ \_ OUTPUT \_ STREAMF OPTIONAL DMO OUTPUT \_ \_ \_ STREAMF. Esses sinalizadores significam quase a mesma coisa; uma pequena diferença entre eles será explicada em breve.

Se um fluxo for opcional, o cliente poderá instruir o DMO a descartar dados desse fluxo quando ele processa a saída. Para fazer isso, chame o método [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) e de definir o buffer de saída como **NULL** para cada fluxo que você deseja descartar. (O buffer de saída é especificado no membro **pBuffer** do [**buffer DMO OUTPUT DATA \_ \_ \_ BUFFER**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer).) Defina também o DMO \_ PROCESS OUTPUT DISCARD WHEN NO BUFFER no parâmetro \_ \_ \_ \_ \_ *dwFlags.*

Para cada fluxo em que *o ponteiro pBuffer* **é NULL,** o DMO tentará descartar os dados. Se o fluxo for opcional, o DMO será garantido para descartar os dados. Se o fluxo não for opcional, o DMO descartará os dados quando possível, mas não há garantia de fazer isso. Se ele não puder descartar os dados, ele define o DMO \_ BUFFER DE DADOS DE \_ \_ SAÍDAF \_ INCOMPLETO. Se você definir um *ponteiro pBuffer* como **NULL,** mas não definir o sinalizador DMO PROCESS OUTPUT DISCARD WHEN NO BUFFER, o DMO \_ não \_ \_ \_ \_ \_ descartará os dados. Nesse caso, o DMO buffer da saída internamente ou simplesmente falha na **chamada ProcessOutput.**

A única diferença funcional entre o sinalizador DMO OUTPUT STREAMF OPTIONAL e o sinalizador \_ \_ DMO OUTPUT \_ \_ \_ STREAMF \_ DISCARDABLE é o seguinte:

-   O DMO OUTPUT STREAMF OPTIONAL indica que o cliente não precisa definir um tipo de \_ \_ mídia nesse \_ fluxo. No entanto, se o cliente começar a processar dados sem definir o tipo de mídia para esse fluxo, ele deverá descartar os dados desse fluxo durante toda a duração do streaming. Se você quiser descartar amostras seletivamente, deverá definir o tipo de mídia.
-   O DMO OUTPUT STREAMF DISCARDABLE indica que, embora o fluxo seja opcional, ele \_ sempre requer um tipo de \_ \_ mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



