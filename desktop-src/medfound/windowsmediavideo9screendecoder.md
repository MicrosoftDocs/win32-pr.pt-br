---
description: O decodificador de tela do Windows Media Video 9 decodifica os fluxos que foram codificados pelo codificador de tela do Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Decodificador de tela do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784521"
---
# <a name="windows-media-video-9-screen-decoder"></a>Decodificador de tela do Windows Media Video 9

O decodificador de tela do Windows Media Video 9 decodifica os fluxos que foram codificados pelo [**codificador de tela do Windows Media Video 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do decodificador de tela do Windows Media Video 9 é representado pela constante **CLSID \_ CMSSCDecMediaObject**. Você pode criar uma instância do decodificador chamando **CoCreateInstance**.

## <a name="input-types"></a>Tipos de entrada

O FOURCC (código de quatro caracteres) para o conteúdo codificado da tela de vídeo do Windows Media versão 9 é "MSS2".

Os seguintes tipos de entrada são suportados pelo decodificador de tela da versão 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Tipos de saída

Os tipos de saída a seguir têm suporte no decodificador de tela da versão 9 quando ele está sendo usado como um objeto de mídia do DirectX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Os tipos de saída a seguir têm suporte no decodificador de tela da versão 9 quando ele está sendo usado como uma Media Foundation transformação (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Comentários

Um objeto decodificador de tela expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um decodificador de tela se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. A tabela a seguir mostra as condições sob as quais um decodificador de tela se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um decodificador de tela do Windows Media sempre se comporta como DMO.                                                                                                                 |
| Windows Vista e Windows 7 | Por padrão, um decodificador de tela do Windows Media se comporta como DMO. Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um decodificador de tela, ela se comporta como um MFT. |



 

Você pode usar o mesmo CLSID (CLSID \_ CMSSCDecMediaObject) para criar o decodificador de tela da versão 7 e o decodificador de tela da versão 9. O FOURCC para o conteúdo codificado da tela de vídeo do Windows Media versão 7 é "MSS1". O decodificador de tela da versão 7 dá suporte ao \_ tipo de entrada MEDIASUBTYPE MSS1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> <dt>

[Usando o codec de tela do Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Codificador de tela do Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
