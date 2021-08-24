---
description: O Windows decodificador de tela Windows Media Video 9 decodifica fluxos que foram codificados pelo codificador de tela Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Decodificador de tela do Vídeo de Mídia 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2e081423c4c5efc2d44fdf78c7c6a94a00dae86d40d761a06ab0de07fa5d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462386"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Decodificador de tela do Vídeo de Mídia 9

O decodificador de tela Windows Media Video 9 decodifica fluxos que foram codificados pelo codificador de tela [**Windows Media Video 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do decodificador de tela Windows Media Video 9 é representado pela constante **CLSID \_ CMSSCDecMediaObject**. Você pode criar uma instância do decodificador chamando **CoCreateInstance**.

## <a name="input-types"></a>Tipos de entrada

O código de quatro caracteres (FOURCC) para Windows conteúdo codificado da Tela de Vídeo de Mídia 9 é "MSS2".

Os seguintes tipos de entrada são suportados pelo decodificador de tela versão 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Tipos de saída

Os seguintes tipos de saída são suportados pelo decodificador de tela versão 9 quando ele está sendo usado como um objeto de mídia directX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Os seguintes tipos de saída são suportados pelo decodificador de tela versão 9 quando ele está sendo usado como uma transformação Media Foundation (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Comentários

Um objeto de decodificador de tela expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia directX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma transformação Media Foundation (MFT).

Um decodificador de tela se comporta como um DMO ou um MFT, dependendo de quais interfaces você obtém e qual versão do Windows está em execução. A tabela a seguir mostra as condições sob as quais um decodificador de tela se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um Windows decodificador de tela de mídia sempre se comporta como um DMO.                                                                                                                 |
| Windows Vista e Windows 7 | Por padrão, um decodificador Windows Tela de Mídia se comporta como um DMO. Se você obter uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um decodificador de tela, ela se comportará como uma MFT. |



 

Você pode usar o mesmo CLSID (CLSID CMSSCDecMediaObject) para criar o decodificador de tela versão 7 e o decodificador de tela versão \_ 9. O conteúdo codificado Windows tela de vídeo de mídia versão 7 é "MSS1". O decodificador de tela versão 7 dá suporte ao tipo de entrada MEDIASUBTYPE \_ MSS1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> <dt>

[Implementação do Codec](codecimplementation.md)
</dt> <dt>

[Usando o codec de tela Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Codificador de tela do Vídeo de Mídia 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
