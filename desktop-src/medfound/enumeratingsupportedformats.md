---
description: Configurando DMOs codec
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configurando DMOs codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4040c0a16c0311d14b0553336e1d9b70a7a6c1fd28a0f01277c955eea55ec7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958326"
---
# <a name="configuring-codec-dmos"></a>Configurando DMOs codec

Este tópico descreve o processo de configuração dos DMOs codec. Cada codec tem procedimentos específicos, mas as informações comuns a todos são descritas aqui.

## <a name="configuring-dmo-inputs-and-outputs"></a>Configurando DMO entradas e saídas

Cada DMO dá suporte a tipos específicos de entrada e saída. Você pode recuperar tipos com suporte para entradas e saídas chamando [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) para entradas e [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) para saídas. Você pode enumerar os formatos com suporte fazendo chamadas repetidas para qualquer método, incrementando o índice de tipo com cada chamada. Quando o índice excede o do tipo final com suporte, a chamada retorna DMO \_ E \_ NO MORE \_ \_ ITEMS.

Para os codecs de vídeo, apenas um tipo de saída ou tipo de entrada é enumerado para um determinado subtipo de mídia. Para os codecs de áudio, cada tipo com suporte individual é enumerado. Para obter mais informações sobre tipos com suporte para codecs individuais, consulte [Trabalhando com áudio](workingwithaudio.md) e trabalhando com [vídeo.](workingwithvideo.md)

Depois de configurar os tipos de mídia para os fluxos de entrada e saída, configure-os chamando [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType,**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) respectivamente. Ambos os métodos retornarão **DMO E TYPE NOT \_ \_ \_ \_ ACCEPTED** se o tipo especificado for inválido.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configurando os DMOs codec para codificação

Todos os codecs Windows áudio de mídia e vídeo são suportados por uma variedade de recursos de codificação. Esses recursos geralmente são configurados definindo propriedades no DMO usando os métodos da interface **IPropertyBag.** Algumas propriedades são configuradas usando interfaces de codec especializadas. Essas interfaces são listadas para cada codec na seção [Objetos codec](codecobjects.md).

A ordem geral das operações para configurar um DMO codificação é a seguinte:

1.  Configure os recursos de codec conforme desejado usando os métodos de **IPropertyBag.**
2.  Use as interfaces de DMO codec para configurar recursos adicionais, se necessário.
3.  Configure os tipos de entrada e saída. A ordem na qual os tipos devem ser configurados varia para codecs individuais. Para obter mais informações, consulte [Trabalhando com áudio e](workingwithaudio.md) trabalhando com [vídeo.](workingwithvideo.md)

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configurando os DMOs codec para decodificação

A decodificação é mais simples do que a codificação, pois há suporte para menos recursos de decodificador.

A ordem geral das operações para configurar um DMO decodificação é a seguinte:

1.  Configure os recursos do decodificador conforme desejado usando os métodos de **IPropertyBag**.
2.  De definir o tipo de entrada para o tipo usado para a saída do codificador.
3.  Configure o tipo de saída. Os tipos de saída com suporte são diferentes para entradas diferentes.

> [!Note]  
> É importante usar o mesmo tipo de mídia para a entrada do decodificador que foi usado para a saída do codificador. Isso porque os codecs Windows Áudio de Mídia e Vídeo usam formatos de mídia com dados extras. Esses dados são acrescentados à estrutura apontada pelo membro **pbFormat** da estrutura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (geralmente [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**WAVEFORMATEX).**](/previous-versions/dd757713(v=vs.85)) Para alguns tipos, os dados extras fazem parte do tipo de saída do codificador enumerado. Outros tipos exigem que você adefina esses dados manualmente. Sem os dados de formato estendido, você não pode decodificar o conteúdo compactado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com DMOs codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
