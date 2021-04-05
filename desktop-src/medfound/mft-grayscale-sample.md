---
description: Mostra como implementar um efeito de vídeo como uma Media Foundation transformação (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Exemplo de MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091051"
---
# <a name="mft_grayscale-sample"></a>Exemplo de escala de cinza da MFT \_

Mostra como implementar um efeito de vídeo como uma Media Foundation transformação (MFT). O MFT em escala de cinza converte o vídeo YUV em escala de cinza definindo os valores de croma no vídeo como neutro. O MFT aceita vídeo descompactado nos formatos UYVY, YUY2 ou NV12.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

O exemplo de escala de cinza do MFT \_ cria uma DLL que é um servidor com para o MFT. Antes de usar o MFT, você deve registrar a DLL.

Para ver o MFT em escala de cinza em uso, execute o [exemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)). Você também pode usar a ferramenta TopoEdit para criar uma topologia que inclui o MFT em tons de cinza. Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o vídeo YUV](about-yuv-video.md)
</dt> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Exemplo de AudioDelay de MFT \_](mft-audiodelay-sample.md)
</dt> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 
