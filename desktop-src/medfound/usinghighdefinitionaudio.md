---
description: Usando High-Definition áudio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Usando High-Definition áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3eac918929b6495401a0eeaee31fe6d7a01d2df0eced9866da829381392edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737329"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Usando High-Definition áudio (Microsoft Media Foundation)

áudio de alta definição, no contexto do Windows codecs de áudio de mídia, é qualquer tipo de áudio com mais de dois canais ou mais de 16 bits por amostra. o áudio de alta definição tem suporte nas categorias Professional e sem perdas do [codificador de áudio Windows Media](windowsmediaaudioencoder.md).

Tipos de áudio de alta definição não compactados são definidos usando a estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) . **WAVEFORMATEXTENSIBLE** é uma extensão estruturada da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . quando você estiver usando DMOs, o membro **formattype** da estrutura [**do \_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que descreve um tipo de áudio de alta definição deve ser definido como WMCFORMAT \_ WaveFormatEx, assim como é para o áudio normal; não há nenhum identificador de formato especial para **WAVEFORMATEXTENSIBLE**. Se um formato usar **WAVEFORMATEXTENSIBLE** , você deverá definir o membro **CbSize** da estrutura **WAVEFORMATEX** como 22.

Ao usar Media Foundation, você pode construir o tipo de mídia correto de uma estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) usando a função [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

os tipos de saída multicanal com suporte no codec Windows Media Audio 10 Professional não usam [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), mas relatam o número correto de canais e bits por amostra na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . assim como acontece com todos os tipos de áudio que descrevem o conteúdo compactado Windows mídia de áudio, há informações adicionais acrescentadas à estrutura **WAVEFORMATEX** que é usada pelo decodificador para descompactação.

## <a name="decoding-high-definition-audio"></a>Decodificando High-Definition áudio

Para decodificar áudio de alta definição, você deve definir a propriedade [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) como Variant \_ true. Se essa propriedade não for definida, o decodificador fornecerá conteúdo estéreo com um máximo de 16 bits por amostra, independentemente do formato compactado.

> [!Note]  
> o áudio de alta definição tem suporte apenas para Windows XP, Windows Vista e posterior. em versões anteriores do Windows, Windows conteúdo de áudio de mídia codificado com alta definição é renderizado como áudio de dois canais com um máximo de 16 bits por amostra.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 
