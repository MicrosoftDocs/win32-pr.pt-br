---
description: Códigos FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Códigos FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25820d21fb8e8386fb11816c373debf427fa783b8a2f2d4723a46e689e6aea0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043316"
---
# <a name="fourcc-codes"></a>Códigos FOURCC

Muitos formatos de mídia digital têm códigos FOURCC atribuídos a eles. Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII. Por exemplo, o código FOURCC para vídeo YUY2 é ' YUY2 '. Para formatos de vídeo compactados e formatos de vídeo não RGB (como YUV), o membro de **bicompressão** da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) deve ser definido como o código FOURCC.

Há várias macros C/C++ que facilitam a declaração de valores FOURCC no código-fonte. Por exemplo, a macro **MAKEFOURCC** é declarada em mmsystem. h e a macro **FCC** é declarada em Aviriff. h. Use-os da seguinte maneira:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



Você também pode declarar um código FOURCC diretamente como um literal de cadeia de caracteres simplesmente revertendo a ordem dos caracteres. Por exemplo:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



a reversão do pedido é necessária porque o sistema operacional Microsoft Windows usa uma arquitetura little-endian. ' Y ' = 0x59, ' U ' = 0x55 e ' 2 ' = 0x32, portanto, ' 2YUY ' é 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Convertendo códigos FOURCC em GUIDs de subtipo

Um intervalo de 2 \* GUIDs de 32 é reservado para representar FOURCC. Esses GUIDs são todos os formulários `XXXXXXXX-0000-0010-8000-00AA00389B71` em que `XXXXXXXX` o código FOURCC é. Portanto, o GUID de subtipo para YUY2 é `32595559-0000-0010-8000-00AA00389B71` .

Muitas dessas GUIDs já estão definidas no arquivo de cabeçalho UUIDs. h. Por exemplo, o subtipo YUY2 é definido como MEDIASUBTYPE \_ YUY2. o DirectShow biblioteca de classes base também fornece uma classe auxiliar, [**FOURCCMap**](fourccmap.md), que pode ser usada para converter códigos FOURCC em valores de GUID. O construtor **FOURCCMap** usa um código FOURCC como um parâmetro de entrada. Em seguida, você pode converter o objeto **FOURCCMap** no GUID correspondente:


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Subtipos de áudio**](audio-subtypes.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabalhando com codecs](working-with-codecs.md)
</dt> </dl>

 

 



