---
description: Aceleração de vídeo do DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Aceleração de vídeo do DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164190"
---
# <a name="directx-video-acceleration-20"></a>Aceleração de vídeo do DirectX 2,0

A DXVA (aceleração de vídeo do DirectX) é uma API e uma DDI correspondente para usar a aceleração de hardware para acelerar o processamento do codec de vídeo. Os codecs de software e os processadores de vídeo de software podem usar o DXVA para descarregar determinadas operações com uso intensivo de CPU para a GPU. Por exemplo, um decodificador de software pode descarregar a transformação de cosseno discreto inverso (iDCT) para a GPU.

Esta seção contém os seguintes tópicos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o DXVA 2,0](about-dxva-2-0.md)<br/>                                                   | Visão geral do DXVA 2 e sua relação com o DXVA 1.<br/>                                                                                                                                                        |
| [Gerenciador de Dispositivos Direct3D](direct3d-device-manager.md)<br/>                                 | O Microsoft Direct3D Device Manager permite que dois ou mais objetos compartilhem o mesmo dispositivo Microsoft Direct3D 9.<br/>                                                                                      |
| [Suporte a DXVA 2,0 no DirectShow](supporting-dxva-2-0-in-directshow.md)<br/>             | Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em um filtro de decodificador do DirectShow.<br/>                                                                                             |
| [Suporte a DXVA 2,0 no Media Foundation](supporting-dxva-2-0-in-media-foundation.md)<br/> | Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em uma Media Foundation transformação (MFT) usando o Direct3D 9<br/>                                                                      |
| [Processamento de vídeo de DXVA](dxva-video-processing.md)<br/>                                     | O processamento de vídeo de DXVA encapsula as funções do hardware de gráficos que são dedicadas ao processamento de imagens de vídeo descompactadas. Os serviços de processamento de vídeo incluem desentrelaçamento e mixagem de vídeo.<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) é uma API para processamento de vídeo acelerado por hardware. <br/>                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Especificação de DXVA 1](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
