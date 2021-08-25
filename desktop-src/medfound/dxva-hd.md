---
description: A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) é uma API para processamento de vídeo acelerado por hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40e23d6e91f576f062c52a0f58d0bfe1f769ad3879581b01386333266cb0553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958646"
---
# <a name="dxva-hd"></a>DXVA-HD

A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) é uma API para processamento de vídeo acelerado por hardware. O DXVA-HD usa a GPU para executar funções como desentrelaçamento, composição e conversão de espaço de cor.

O DXVA-HD é semelhante ao [processamento de vídeo de DXVA](dxva-video-processing.md) (DXVA-VP), mas oferece recursos avançados e um modelo de processamento mais simples. Ao fornecer um modelo de composição mais flexível, o DXVA-HD foi projetado para dar suporte à próxima geração de formatos ópticos de HD e padrões de difusão.

A API de DXVA-HD requer um driver de vídeo WDDM que dá suporte à DDI (interface de driver de dispositivo) de DXVA-HD ou um processador de software de plug-in.

-   [Melhorias em relação a DXVA-VP](#improvements-over-dxva-vp)
-   [Tópicos relacionados](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Melhorias em relação a DXVA-VP

DXVA-HD expande o conjunto de recursos fornecidos pelo DXVA-VP. Os aprimoramentos incluem:

-   Mixagem de RGB e YUV. Qualquer fluxo pode ser RGB ou YUV. Não há mais uma distinção entre o fluxo principal e os subfluxos.
-   Desentrelaçamento de vários fluxos. Qualquer fluxo pode ser progressivo ou entrelaçado. Além disso, a cadência e a taxa de quadros podem variar de um fluxo de entrada para o outro.
-   Cores de fundo RGB. Anteriormente, há suporte apenas para cores de plano de fundo YUV.
-   Luma de chave. Quando o Luma de chaveamento está habilitado, os valores de Luma que se enquadram em um intervalo designado tornam-se transparentes
-   Alternância dinâmica entre os modos de desentrelaçamento.

O DXVA-HD também define alguns recursos avançados aos quais os drivers podem dar suporte. No entanto, os aplicativos não devem pressupor que todos os drivers oferecerão suporte a esses recursos. Os recursos avançados incluem:

-   Telecineon inverso (por exemplo, 60i para 24p).
-   Conversão de taxa de quadros (por exemplo, 24p para 120P).
-   Modos de preenchimento alfa.
-   Redução de ruído e filtragem de aprimoramento de borda.
-   Anamorphic dimensionamento não linear.
-   YCbCr estendido (xvYCC).

Esta seção contém os seguintes tópicos.

-   [Criando um processador de vídeo de DXVA-HD](creating-a-dxva-hd-video-processor.md)
-   [Verificando os formatos de DXVA-HD com suporte](checking-supported-dxva-hd-formats.md)
-   [Criando superfícies de vídeo de DXVA-HD](creating-dxva-hd-video-surfaces.md)
-   [Definindo Estados de DXVA-HD](setting-dxva-hd-states.md)
-   [Executando o blit DXVA-HD](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Exemplo de DXVA-HD](dxva-hd-sample.md)
</dt> </dl>

 

 



