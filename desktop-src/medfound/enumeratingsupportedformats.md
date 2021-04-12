---
description: Configurando o codec DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configurando o codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564c0e6c566d9f583a495238f3ea6f0716d7adde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457215"
---
# <a name="configuring-codec-dmos"></a>Configurando o codec DMOs

Este tópico descreve o processo de configuração do codec DMOs. Cada codec tem procedimentos específicos, mas as informações comuns a todos são descritas aqui.

## <a name="configuring-dmo-inputs-and-outputs"></a>Configurando entradas e saídas de DMO

Cada DMO dá suporte a tipos de entrada e saída específicos. Você pode recuperar tipos com suporte para entradas e saídas chamando [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) para inputs e [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) para saídas. Você pode enumerar os formatos com suporte fazendo chamadas repetidas para qualquer método, incrementando o índice de tipo com cada chamada. Quando o índice excede a do tipo com suporte final, a chamada retorna DMO \_ E \_ não \_ mais \_ itens.

Para os codecs de vídeo, apenas um tipo de saída ou tipo de entrada é enumerado para um determinado subtipo de mídia. Para os codecs de áudio, cada tipo com suporte individual é enumerado. Para obter mais informações sobre os tipos com suporte para codecs individuais, consulte [trabalhando com áudio](workingwithaudio.md) e [trabalhando com vídeo](workingwithvideo.md).

Depois de configurar os tipos de mídia para os fluxos de entrada e saída, defina-os chamando [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) , respectivamente. Ambos os métodos retornam **o \_ tipo DMO E \_ não são \_ \_ aceitos** se o tipo especificado é inválido.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configurando o codec DMOs para codificação

Todos os codecs de vídeo e áudio do Windows Media oferecem suporte a uma variedade de recursos de codificação. Esses recursos geralmente são configurados definindo as propriedades no DMO usando os métodos da interface **IPropertyBag** . Algumas propriedades são configuradas usando interfaces de codec especializadas. Essas interfaces são listadas para cada codec na seção [objetos de codec](codecobjects.md).

A ordem geral das operações para configurar uma codificação DMO é a seguinte:

1.  Configure os recursos de codec conforme desejado usando os métodos de **IPropertyBag**.
2.  Use as interfaces do codec DMO para configurar recursos adicionais, se necessário.
3.  Configure os tipos de entrada e saída. A ordem na qual os tipos devem ser configurados varia de acordo com os codecs individuais. Para obter mais informações, consulte [trabalhando com áudio](workingwithaudio.md) e [trabalhando com vídeo](workingwithvideo.md).

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configurando o codec DMOs para decodificação

A decodificação é mais simples do que a codificação, pois há suporte para menos recursos de decodificador.

A ordem geral das operações para configurar uma decodificação DMO é a seguinte:

1.  Configure os recursos do decodificador conforme desejado usando os métodos de **IPropertyBag**.
2.  Defina o tipo de entrada para o tipo usado para a saída do codificador.
3.  Configure o tipo de saída. Os tipos de saída com suporte são diferentes para entradas diferentes.

> [!Note]  
> É importante usar o mesmo tipo de mídia para a entrada do decodificador como foi usado para a saída do codificador. Isso ocorre porque os codecs de áudio e vídeo do Windows Media usam formatos de mídia com dados adicionais. Esses dados são anexados à estrutura apontada pelo membro **pbFormat** da estrutura do [**tipo de \_ mídia \_ DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (geralmente [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))). Para alguns tipos, os dados adicionais fazem parte do tipo de saída do codificador enumerado. Outros tipos exigem que você acrescente esses dados manualmente. Sem os dados de formato estendidos, você não pode decodificar o conteúdo compactado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
