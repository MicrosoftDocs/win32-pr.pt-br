---
description: o decodificador Windows Media mpeg-4 v3 decodifica fluxos de vídeo mpeg-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Decodificador de mídia MPEG-4 v3 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975351d04b0876b5f1793d442e41d54a585062bd1fed778902fee5c4c83dcd6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100908"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Decodificador de mídia MPEG-4 v3

o decodificador Windows Media mpeg-4 v3 decodifica fluxos de vídeo mpeg-4 v3.

## <a name="class-identifier"></a>Identificador de classe

o clsid (identificador de classe) para o decodificador Windows MPEG-4 V3 é representado pela constante **CLSID \_ CMpeg43DecMediaObject**. Você pode criar uma instância do decodificador MPEG-4 v3 chamando **CoCreateInstance**.

## <a name="formats"></a>Formatos

o decodificador Windows media MPEG-4 V3 dá suporte aos seguintes tipos de mídia de entrada.

-   MEDIASUBTYPE \_ MP43
-   MEDIASUBTYPE \_ mp43

o decodificador Windows media MPEG-4 V3 dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como um objeto de mídia do DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

o decodificador de mídia MPEG-4 V3 do Windows dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como uma Media Foundation transformação (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Comentários

o objeto decodificador do Windows media MPEG-4 V3 expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT). o objeto tem o mesmo identificador de classe (CLSID), independentemente de agir como um DMO ou um MFT.

o decodificador MPEG-4 V3 se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está em execução. a tabela a seguir mostra as condições sob as quais um decodificador MPEG-4 V3 se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | O decodificador MPEG-4 v3 sempre se comporta como um DMO.                                                                                                                      |
| Windows Vista e Windows 7 | Por padrão, o decodificador MPEG-4 v3 se comporta como um DMO. Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) no decodificador MPEG-4 v3, ele se comporta como um MFT. |



 

os identificadores globalmente exclusivos (guids) para subtipos de mídia RGB diferem dependendo se um decodificador está agindo como um DMO ou um MFT. os guids para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar agindo como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
