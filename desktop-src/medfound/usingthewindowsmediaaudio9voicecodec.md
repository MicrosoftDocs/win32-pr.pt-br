---
description: Usando o codec de voz de áudio do Windows Media
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Usando o codec de voz de áudio do Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506332"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Usando o codec de voz de áudio do Windows Media

O codec de voz de áudio do Windows Media fornece compactação de baixa taxa de bits otimizada para áudio contendo fala. A capacidade do codec de produzir esses pequenos exemplos é devido ao intervalo de frequência limitada dos sons da voz humana. Essa otimização significa que um codificador de voz dedicado cria uma saída de baixa qualidade para o conteúdo que contém sons mais complicados, como música. No entanto, o codec de voz de áudio do Windows Media compensa esse possível problema de qualidade fornecendo modos separados para voz, música e conteúdo misto. O codec analisa o conteúdo misto para determinar qual modo usar para cada parte do arquivo.

O codec de voz do Windows Media Audio é implementado no objeto do codificador identificado pelo CLSID do identificador de classe \_ CWMSPEncMediaObject2 e no objeto decodificador identificado pelo CLSID do identificador de classe \_ CWMSPDecMediaObject. A marca de formato dos tipos de mídia usando esse codec é 0x00a.

## <a name="configuring-the-encoder"></a>Configurando o codificador

O codificador de voz dá suporte a três modos: fala, música e misto. Cada modo é otimizado para obter os melhores resultados para esse tipo de conteúdo. Você pode configurar o modo do codificador de voz usando os métodos de **IPropertyStore** para definir a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .

Quando configurado para conteúdo misto, o codec de voz de áudio do Windows Media detectará automaticamente passagens de música no conteúdo. Se você não estiver satisfeito com os resultados, poderá especificar o local de música no conteúdo usando uma EDL (lista de decisões de edição). Para obter mais informações, consulte [usando uma lista de decisões de edição para codificação de voz](usingavoiceeditingdecisionlist.md).

Ao contrário dos outros codificadores de áudio, você pode definir o valor da janela de buffer para o conteúdo de voz usando a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) . No entanto, os valores padrão devem funcionar bem na maioria dos casos.

> [!Note]  
>    Ao configurar o codificador de voz, é muito importante que você defina o tipo de saída antes de definir o tipo de entrada. Essa é a ordem recomendada de operações para todos os codecs de áudio, mas o codificador de voz pode relatar tipos de saída incorretos se uma entrada for definida quando você chamar **IMediaObject:: GetOutputType** ou **IMFTransform:: GetOutputType**.

 

## <a name="decoding"></a>Decodificação

Não há requisitos especiais para decodificar áudio de voz. Para obter mais informações, consulte [Configurando a decodificação de áudio](configuringaudiodecoding.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 



