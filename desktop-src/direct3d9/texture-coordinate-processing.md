---
description: O diagrama a seguir mostra o caminho feito pelas coordenadas de textura de sua origem, por meio de processamento e para o rasterizador.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Processamento de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a161d3675a5859702368a62719124aa029ee455
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010042"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Processamento de coordenadas de textura (Direct3D 9)

O diagrama a seguir mostra o caminho feito pelas coordenadas de textura de sua origem, por meio de processamento e para o rasterizador.

![diagrama do caminho para coordenadas de textura de uma origem para o rasterizador](images/tex-processing.png)

Há duas fontes das quais o sistema pode desenhar coordenadas de textura. Para um determinado estágio de textura, você pode usar as coordenadas de textura incluídas no formato de vértice (D3DFVF \_ TEX1 até D3DFVF \_ TEX8) ou pode usar coordenadas de textura geradas automaticamente pelo Direct3D. Para obter detalhes sobre o último caso, consulte [coordenadas de textura geradas automaticamente (Direct3D 9)](automatically-generated-texture-coordinates.md). Se o \_ estado de estágio de textura D3DTSS TEXTURETRANSFORMFLAGS para o estágio de textura atual for definido como \_ desativação de D3DTTFF (a configuração padrão), as coordenadas de entrada não serão transformadas. Se D3DTSS \_ TEXTURETRANSFORMFLAGS> for definido como qualquer outro valor, a matriz de transformação desse estágio será aplicada às coordenadas de entrada.

O tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) define valores válidos para o estado de D3DTSS de \_ textura de TEXTURETRANSFORMFLAGS. Com exceção do \_ sinalizador de desabilitação D3DTTFF, que ignora a transformação de coordenadas de textura, os valores definidos nessa enumeração configuram o número de coordenadas de saída que o sistema passa para o rasterizador. Os \_ sinalizadores D3DTTFF COUNT1 a D3DTTFF \_ COUNT4 instruem o sistema a passar um, dois, três ou quatro elementos das coordenadas de saída para o rasterizador.

O \_ sinalizador projetado D3DTTFF é especial: ele diz ao sistema que as coordenadas de textura são para uma textura projetada. Combine o \_ sinalizador projetado D3DTTFF com outro membro de [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) para instruir o rasterizador a dividir todos os elementos pelo último elemento antes que a rasterização ocorra. Por exemplo, ao usar explicitamente as coordenadas de textura de três elementos ou quando a transformação resulta em uma coordenada de textura de três elementos, você pode combinar os \_ sinalizadores projetados D3DTTFF COUNT3 e D3DTTFF \_ para fazer com que o rasterizador divida os dois primeiros elementos pela última, produzindo coordenadas de textura 2D necessárias para resolver uma textura 2D.

> [!Note]  
> Com exceção de mapas de ambiente cúbico e texturas de volume, os rasterizadores não podem resolver texturas usando coordenadas de textura com mais de dois elementos. Se você especificar mais elementos do que pode ser usado para endereçar a textura atual para esse estágio, os elementos estranhos serão ignorados. Isso também se aplica ao usar coordenadas de textura 2D para uma textura 1D.

 

Informações adicionais estão contidas nos tópicos a seguir.

-   [Coordenadas de textura geradas automaticamente (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformações de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md)
-   [Efeitos especiais (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 
