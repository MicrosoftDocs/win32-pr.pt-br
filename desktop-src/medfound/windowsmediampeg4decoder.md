---
description: O Windows decodificador MPEG4 V1/V2 decodifica fluxos de vídeo MPEG4 V1/V2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Decodificador MPEG4 V1/V2 de mídia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c55d5c64cec2a0ad08978064d40c26267d7729adeee9a9f148c8e682ba168509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100928"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Windows Decodificador MPEG4 V1/V2 de mídia

O Windows decodificador MPEG4 V1/V2 decodifica fluxos de vídeo MPEG4 V1/V2.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) para o decodificador MPEG4 V1/V2 da mídia Windows é representado pela constante **CLSID \_ CMpeg4DecMediaObject**. Você pode criar uma instância do decodificador MPEG4 V1/V2 chamando **CoCreateInstance**.

## <a name="formats"></a>Formatos

O decodificador Windows Mídia MPEG4 V1/V2 dá suporte aos seguintes tipos de mídia de entrada.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ mpg4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ mp42

O decodificador mpeg4 V1/V2 da mídia de Windows de saída dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um objeto de mídia directX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

O decodificador Windows Mídia MPEG4 V1/V2 dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como uma transformação Media Foundation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Comentários

O objeto decodificador MPEG4 V1/V2 de mídia do Windows expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um Objeto de Mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma transformação Media Foundation (MFT). O objeto tem o mesmo CLSID (identificador de classe), independentemente de atuar como um DMO ou um MFT.

Um decodificador MPEG4 V1/V2 se comporta como um DMO ou um MFT, dependendo de quais interfaces você obtém e qual versão do Windows está em execução. A tabela a seguir mostra as condições sob as quais um decodificador MPEG4 V1/V2 se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um decodificador MPEG4 V1/V2 sempre se comporta como um DMO.                                                                                                                                 |
| Windows Vista e Windows 7 | Por padrão, um decodificador MPEG4 V1/V2 se comporta como um DMO. Se você obter uma interface [GUIDs](video-subtype-guids.md) de subtipo de vídeo em um decodificador MPEG4 V1/V2, ele se comportará como uma MFT. |



 

Os GUIDs (identificadores globalmente exclusivos) para subtipos de mídia RGB diferem dependendo se um decodificador está atuando como um DMO ou um MFT. Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar atuando como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de vídeo, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> </dl>

 

 
