---
description: Saiba mais sobre a mistura alfa. A mesclagem alfa é usada para exibir uma imagem que tem pixels transparentes ou semi-transparente.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Mistura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261998"
---
# <a name="alpha-blending-direct3d-9"></a>Mistura alfa (Direct3D 9)

A mesclagem alfa é usada para exibir uma imagem que tem pixels transparentes ou semi-transparente. Além de um canal de cores vermelho, verde e azul, cada pixel em um bitmap alfa tem um componente de transparência conhecido como seu canal alfa. Normalmente, o canal alfa contém tantos bits quanto um canal de cores. Por exemplo, um canal alfa de 8 bits pode representar 256 níveis de transparência, de 0 (o pixel inteiro é transparente) a 255 (o pixel inteiro é opaco). A lista a seguir mostra alguns efeitos especiais que você pode criar usando a mistura alfa.

A cor pode ser definida com ou sem valores Alfa. Color sem alfa é a cor RGB com alfa é armazenada como ARGB. Dados de vértice, dados de material e dados de textura podem ser usados para fornecer transparência do objeto. O buffer de quadros também pode ser usado para gerar efeitos de transparência.

-   [Vértice alfa (Direct3D 9)](vertex-alpha.md)
-   [Material alfa (Direct3D 9)](material-alpha.md)
-   [Textura alfa (Direct3D 9)](texture-alpha.md)
-   [Buffer de quadro alfa (Direct3D 9)](frame-buffer-alpha.md)
-   [Processamento alfa de destino (Direct3D 9)](render-target-alpha.md)

Exemplos que demonstram alfa incluem:

-   [Mural (Direct3D 9)](billboarding.md)
-   [Nuvens, fumaça e trilhas Vapors (Direct3D 9)](clouds--smoke--and-vapor-trails.md)
-   [Fogo, flares e explosões (Direct3D 9)](fire--flares--and-explosions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



