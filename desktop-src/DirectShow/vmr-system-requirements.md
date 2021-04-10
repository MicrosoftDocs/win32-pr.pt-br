---
description: Requisitos do sistema do VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Requisitos do sistema do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170263"
---
# <a name="vmr-system-requirements"></a>Requisitos do sistema do VMR

O VMR usa exclusivamente os recursos de processamento de gráficos do cartão de vídeo do computador; o VMR não executa nenhuma mistura ou renderização de vídeo usando o processador do host, pois isso afetaria muito a taxa de quadros e a qualidade do vídeo que está sendo exibido. Ao aproveitar os novos recursos oferecidos pelo VMR, particularmente mesclagem de vários fluxos de vídeo e/ou imagens de aplicativos, o desempenho geral obtido é altamente dependente dos recursos da placa gráfica que está sendo usada no computador. As placas gráficas que executam bem com o VMR têm o seguinte suporte de hardware interno:

-   Suporte para superfícies de textura de Direct3D e "sem energia de 2".
-   A capacidade de StretchBlt das superfícies de YUV para RGB do DirectDraw.
-   Pelo menos 16MB de memória de vídeo se vários fluxos de vídeo forem mesclados juntos. A quantidade real de memória necessária depende do tamanho da imagem dos fluxos de vídeo e da resolução do modo de exibição que está sendo usado.
-   Suporte para uma sobreposição RGB ou a capacidade de misturar para uma superfície de sobreposição YUV.
-   Vídeo acelerado por hardware (suporte para aceleração de vídeo do DirectX) decodificação.
-   Taxas de preenchimento de pixel alto.

> [!Note]  
> O VMR requer que o monitor do sistema seja definido para uma profundidade de cor de pelo menos 16 bits. O VMR não poderá ser colocado em um estado de execução se o monitor estiver definido para 256 cores. Além disso, algumas placas de vídeo não podem executar operações de Direct3D quando a exibição é definida como 24 bits por pixel.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o processamento de mixagem de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



