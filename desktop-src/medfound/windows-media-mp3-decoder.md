---
description: O Windows decodificador media MP3 decodifica arquivos de áudio que foram codificados nos formatos a seguir.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Decodificador mp3 de mídia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58788a00ddaa43686c3cb4be4a52292edb3fe6c6f81fabbc5b4f3e75c47f0f24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736995"
---
# <a name="windows-media-mp3-decoder"></a>Windows Decodificador mp3 de mídia

O Windows decodificador media MP3 decodifica arquivos de áudio que foram codificados nos formatos a seguir.

-   ISO/IEC 11172-3 (ÁUDIO MPEG-1) Camada 3
-   ISO/IEC 13818-3 (ÁUDIO MPEG-2) Camada 3, extensão de baixa frequência de amostragem

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do decodificador Windows Media MP3 é representado pela constante **CLSID \_ CMP3DecMediaObject**. Você pode criar uma instância do decodificador MP3 chamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Um objeto de decodificador MP3 expõe a interface **IMediaObject** para que o objeto possa ser usado como um Objeto de Mídia DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma transformação Media Foundation (MFT).

Um decodificador Windows Media MP3 se comporta como um DMO ou um MFT, dependendo de quais interfaces você obtém e qual versão do Windows está em execução. A tabela a seguir mostra as condições sob as quais um decodificador mp3 de mídia Windows se comporta como um DMO ou um MFT.



| Sistema operacional | Comportamento do decodificador                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Um Windows decodificador mp3 de mídia sempre se comporta como um DMO.                                                                                                                                           |
| Windows Vista    | Por padrão, um decodificador Windows Media MP3 se comporta como um DMO. Se você obter uma interface **IMFTransform** ou uma interface **IPropertyStore** em um decodificador de mp3 de mídia Windows, ele se comportará como uma MFT. |
| Windows 7        | Por padrão, um decodificador Windows Media MP3 se comporta como um DMO. Se você obter uma interface **IMFTransform** em um decodificador mp3 de mídia Windows, ele se comportará como um MFT.                                    |



 

## <a name="input-formats"></a>Formatos de entrada

A tabela a seguir mostra a marca de formato de áudio que representa o tipo de entrada com suporte pelo decodificador Windows Media MP3.



| Constante de marca de formato      | Valor da marca de formato | Formato de áudio     |
|--------------------------|------------------|------------------|
| FORMATO \_ WAVE \_ MPEGLAYER3 | 0x55             | Camada 3 do MPEG ISO |



 

## <a name="output-formats"></a>Formatos de saída

A tabela a seguir mostra as marcas de formato de áudio que representam os tipos de saída com suporte pelo decodificador Windows Media MP3.



| Constante de marca de formato       | Valor da marca de formato | Formato de áudio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| FORMATO WAVE \_ \_ PCM         | 0x0001           | Formato PCM (quando usado como um DMO ou um MFT)                                   |
| WAVE \_ FORMAT \_ IEEE \_ FLOAT | 0x0003           | Ponto flutuante IEEE (quando usado como um MFT)                                   |
| FORMATO \_ WAVE \_ EXTENSÍVEL  | 0xFFFE           | Formato PCM/IEEE na **estrutura WAVEFORMATEXTENSIBLE** (quando usado como um MFT) |



 

O decodificador Windows Media MP3 dá suporte e enumera os seguintes tipos de mídia de saída.

-   Um tipo de saída que tem a mesma taxa de amostragem e número de canais que o tipo de entrada.
-   Saída mono para entrada estéreo.
-   Tipos de saída com profundidades de bits de 8 e 16.
-   Saída de ponto flutuante, se o decodificador estiver se comportando como um MFT.

O decodificador Windows Media MP3 dá suporte, mas não enumera, os seguintes tipos de mídia de saída.

-   Um tipo de saída que tem metade da taxa de amostragem do tipo de entrada.
-   Um tipo de saída que tem um quarto da taxa de amostragem do tipo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> <dt>

[Implementação do Codec](codecimplementation.md)
</dt> </dl>

 

 




