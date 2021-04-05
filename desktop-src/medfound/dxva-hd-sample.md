---
description: Mostra como usar o Microsoft DirectX vídeo Acceleration High Definition (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Exemplo de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826731"
---
# <a name="dxva-hd-sample"></a>Exemplo de DXVA-HD

Mostra como usar o Microsoft DirectX vídeo Acceleration High Definition (DXVA-HD).

Esse exemplo é essencialmente uma porta do [exemplo de \_ VideoProc DXVA2](dxva2-videoproc-sample.md). Ele tem as mesmas funções básicas e a maioria dos comandos de teclado é a mesma.

O exemplo gera programaticamente vídeo com um fluxo primário e um subfluxo. O fluxo primário exibe barras de cores SMPTE. O Subfluxo é misturado no fluxo principal usando Luma de chave. O usuário pode alterar os parâmetros de processamento de vídeo, incluindo o valor alfa do planar, os retângulos de origem e de destino, os ajustes de cor e o espaço de cores. A imagem a seguir mostra o vídeo que é gerado.

![captura de tela do exemplo de DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de DXVA-HD:

-   [**\_Dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



