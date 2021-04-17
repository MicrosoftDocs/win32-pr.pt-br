---
description: As imagens 3D geradas por computador antigamente, embora geralmente avançadas para o tempo, tendiam a ter uma aparência de plástico brilhante.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Conceitos básicos de texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761208"
---
# <a name="basic-texturing-concepts-direct3d-9"></a>Conceitos básicos de texturing (Direct3D 9)

As imagens 3D geradas por computador antigamente, embora geralmente avançadas para o tempo, tendiam a ter uma aparência de plástico brilhante. Eles não tinham os tipos de marcações como arranhões, rachaduras, impressões digitais e manchas da tela que dão aos objetos 3D uma complexidade visual realística. Nos últimos anos, as texturas ganharam popularidade entre os desenvolvedores como uma ferramenta para aprimorar o realm de imagens 3D geradas por computador.

No seu uso diário, a textura word se refere à suavidade ou aspereza de um objeto. Em gráficos de computador, no entanto, uma textura será um bitmap de cores de pixels que dá a aparência de textura de um objeto.

Como as texturas do Direct3D são bitmaps, qualquer bitmap pode ser aplicado a uma primitiva do Direct3D. Por exemplo, os apps podem criar e tratar os objetos que aparecem com um padrão de madeira neles. Grama, sujeira e rochas podem ser aplicadas a um conjunto de primitivas 3D que formam uma colina. O resultado é uma colina realista. Você também pode usar a textura para criar efeitos como sinais ao longo de um acostamento, estratos de rocha em um penhasco, ou a aparência de mármore no chão.

Além disso, o Direct3D dá suporte a técnicas mais avançadas de texturização como a mesclagem de textura com ou sem transparência e o mapeamento de luz. Para obter mais informações, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md) e o [mapeamento claro com texturas (Direct3D 9)](light-mapping-with-textures.md).

Se seu app criar um dispositivo de camada de abstração de hardware (HAL) ou um dispositivo de software, ele pode usar texturas de 8, 16, 24, 32, 64 ou 128 bits.

Informações adicionais estão contidas nos tópicos a seguir.

-   [Modos de endereçamento de textura (Direct3D 9)](texture-addressing-modes.md)
-   [Regiões com problemas de textura (Direct3D 9)](texture-dirty-regions.md)
-   [Paletas de textura (Direct3D 9)](texture-palettes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



