---
description: O decodificador do Windows Media MPEG4 V1/V2 decodifica fluxos de vídeo MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Decodificador do Windows Media MPEG4 V1/V2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105798028"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Decodificador do Windows Media MPEG4 V1/V2

O decodificador do Windows Media MPEG4 V1/V2 decodifica fluxos de vídeo MPEG4 v1/v2.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) para o decodificador MPEG4 v1/v2 do Windows Media é representado pela constante **CLSID \_ CMpeg4DecMediaObject**. Você pode criar uma instância do decodificador MPEG4 V1/V2 chamando **CoCreateInstance**.

## <a name="formats"></a>Formatos

O decodificador MPEG4 v1/v2 do Windows Media dá suporte aos seguintes tipos de mídia de entrada.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ mp42

O decodificador do Windows Media MPEG4 V1/V2 dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como um DMO (objeto de mídia do DirectX).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

O decodificador do Windows Media MPEG4 V1/V2 dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como uma Media Foundation transformação (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Comentários

O objeto decodificador do Windows Media MPEG4 V1/V2 expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT). O objeto tem o mesmo identificador de classe (CLSID), independentemente de atuar como um DMO ou MFT.

Um decodificador MPEG4 V1/V2 se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está em execução. A tabela a seguir mostra as condições sob as quais um decodificador MPEG4 V1/V2 se comporta como DMO ou MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um decodificador MPEG4 V1/V2 sempre se comporta como DMO.                                                                                                                                 |
| Windows Vista e Windows 7 | Por padrão, um decodificador MPEG4 V1/V2 se comporta como DMO. Se você obtiver uma interface de [GUIDs de subtipo de vídeo](video-subtype-guids.md) em um decodificador MPEG4 V1/V2, ele se comporta como um MFT. |



 

Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um decodificador está agindo como um DMO ou um MFT. Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar agindo como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de vídeo, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
