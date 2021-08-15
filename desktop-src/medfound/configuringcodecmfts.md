---
description: Configurando o codec MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configurando o codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb4a9ae53c0aee61e30fb5d61b2ad78fd4fe8e624df394f462dd01618272476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743328"
---
# <a name="configuring-codec-mfts"></a>Configurando o codec MFTs

Este tópico descreve o processo de configuração do codec MFTs. Cada codec tem procedimentos específicos, mas as informações comuns a todos são descritas aqui.

## <a name="configuring-mft-inputs-and-outputs"></a>Configurando entradas e saídas de MFT

Cada MFT dá suporte a tipos específicos de entrada e saída. Você pode recuperar tipos de entrada com suporte chamando repetidamente [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementando o índice de tipo com cada chamada. Quando você encontrar um tipo apropriado, defina o tipo de entrada chamando [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype). Em seguida, você pode repetir o processo para o tipo de saída usando as chamadas [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) e [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Você deve consultar ou definir os tipos de saída disponíveis somente depois de definir o tipo de entrada.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Configurando o codec MFTs para codificação

todos os Windows codecs de áudio e vídeo de mídia dão suporte a uma variedade de recursos de codificação. Esses recursos geralmente são configurados definindo as propriedades no MFT usando os métodos da interface **IPropertyStore** . Algumas propriedades são configuradas usando interfaces de codec especializadas. Essas interfaces são listadas para cada codec na seção [objetos de codec](codecobjects.md).

A ordem geral das operações para configurar uma MFT de codificação é a seguinte:

1.  Configure os recursos de codec conforme desejado usando os métodos de **IPropertyStore**.
2.  Use as interfaces de MFT do codec para configurar recursos adicionais, se necessário.
3.  Configure os tipos de entrada e saída. A ordem na qual os tipos devem ser configurados varia de acordo com os codecs individuais. Para obter mais informações, consulte [trabalhando com áudio](workingwithaudio.md) e [trabalhando com vídeo](workingwithvideo.md).

## <a name="configuring-the-codec-mfts-for-decoding"></a>Configurando o codec MFTs para decodificação

A decodificação é mais simples do que a codificação, pois há suporte para menos recursos de decodificador.

A ordem geral das operações para configurar uma MFT de decodificação é a seguinte:

1.  Configure os recursos do decodificador conforme desejado usando os métodos de **IPropertyStore**.
2.  Defina o tipo de entrada para o tipo usado para a saída do codificador.
3.  Configure o tipo de saída. Os tipos de saída com suporte são diferentes para entradas diferentes.

> [!Note]  
> É importante usar o mesmo tipo de mídia para a entrada do decodificador como foi usado para a saída do codificador. isso ocorre porque os Windows codecs de áudio e vídeo de mídia usam formatos de mídia com dados adicionais. Sem os dados de formato estendidos, você não pode decodificar o conteúdo compactado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



