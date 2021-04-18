---
description: O decodificador MP3 do Windows Media decodifica os arquivos de áudio que foram codificados nos formatos a seguir.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Decodificador MP3 do Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763488"
---
# <a name="windows-media-mp3-decoder"></a>Decodificador MP3 do Windows Media

O decodificador MP3 do Windows Media decodifica os arquivos de áudio que foram codificados nos formatos a seguir.

-   ISO/IEC 11172-3 (áudio MPEG-1) camada 3
-   ISO/IEC 13818-3 (MPEG-2 Audio) camada 3, extensão de frequência de amostragem baixa

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) para o decodificador MP3 do Windows Media é representado pela constante **CLSID \_ CMP3DecMediaObject**. Você pode criar uma instância do decodificador MP3 chamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Um objeto de decodificador MP3 expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um decodificador MP3 do Windows Media se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. A tabela a seguir mostra as condições sob as quais um decodificador MP3 do Windows Media se comporta como um DMO ou um MFT.



| Sistema operacional | Comportamento do decodificador                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Um decodificador MP3 do Windows Media sempre se comporta como DMO.                                                                                                                                           |
| Windows Vista    | Por padrão, um decodificador MP3 do Windows Media se comporta como DMO. Se você obtiver uma interface **IMFTransform** ou uma interface **IPropertyStore** em um decodificador mp3 do Windows Media, ela se comporta como um MFT. |
| Windows 7        | Por padrão, um decodificador MP3 do Windows Media se comporta como DMO. Se você obtiver uma interface **IMFTransform** em um decodificador mp3 do Windows Media, ele se comporta como um MFT.                                    |



 

## <a name="input-formats"></a>Formatos de entrada

A tabela a seguir mostra a marca de formato de áudio que representa o tipo de entrada suportado pelo decodificador MP3 do Windows Media.



| Formatar constante de marca      | Formatar valor da marca | Formato de áudio     |
|--------------------------|------------------|------------------|
| \_MPEGLAYER3 de formato Wave \_ | 0x55             | ISO MPEG camada 3 |



 

## <a name="output-formats"></a>Formatos de saída

A tabela a seguir mostra as marcas de formato de áudio que representam os tipos de saída com suporte pelo decodificador MP3 do Windows Media.



| Formatar constante de marca       | Formatar valor da marca | Formato de áudio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| \_PCM de formato Wave \_         | 0x0001           | Formato PCM (quando usado como um DMO ou MFT)                                   |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Ponto flutuante IEEE (quando usado como um MFT)                                   |
| \_formato Wave \_ extensível  | 0xFFFE           | Formato PCM/IEEE na estrutura **WAVEFORMATEXTENSIBLE** (quando usado como um MFT) |



 

O decodificador MP3 do Windows Media dá suporte e enumera os seguintes tipos de mídia de saída.

-   Um tipo de saída que tem a mesma taxa de amostragem e número de canais que o tipo de entrada.
-   Saída mono para entrada de estéreo.
-   Tipos de saída com profundidades de bits de 8 e 16.
-   Saída de ponto flutuante, se o decodificador estiver se comportando como um MFT.

O decodificador MP3 do Windows Media dá suporte a, mas não enumera, os seguintes tipos de mídia de saída.

-   Um tipo de saída que tem metade da taxa de amostragem do tipo de entrada.
-   Um tipo de saída que tem um quarto da taxa de amostragem do tipo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 




