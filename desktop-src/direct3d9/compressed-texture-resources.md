---
description: Os mapas de textura são imagens digitalizadas desenhadas em formas tridimensionais para adicionar detalhes visuais.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Recursos de textura compactada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd4e21dfd0e042f8d8d97fd8415529a2b4a5a952334df3e7f39ef8ae20a890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989276"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Recursos de textura compactada (Direct3D 9)

Os mapas de textura são imagens digitalizadas desenhadas em formas tridimensionais para adicionar detalhes visuais. Elas são mapeadas para essas formas durante a rasterização, e o processo pode consumir grandes quantidades de memória e barramento de sistema. Para reduzir a quantidade de memória consumida pelas texturas, o Direct3D dá suporte à compactação de superfícies de textura. Alguns dispositivos Direct3D têm suporte nativo às superfícies de textura compactadas. Em tais dispositivos, quando você cria uma superfície compactada e carrega os dados nela, a superfície pode ser usada no Direct3D como qualquer outra superfície de textura. O Direct3D manipula a descompactação quando a textura é mapeada para um objeto 3D.

## <a name="storage-efficiency-and-texture-compression"></a>Armazenamento Eficiência e compactação de textura

Todos os formatos de compactação de textura são potências de dois. Embora isso não signifique que uma textura é necessariamente quadrada, significa que x e y são potências de dois. Por exemplo, se uma textura for originalmente de 512 por 128 bytes, o próximo mapeamento de MIP seria de 256 por 64 e assim por diante, com cada nível diminuindo por uma potência de dois. Em níveis inferiores, onde a textura é filtrada como 16 por 2 e 8 por 1, haverá desperdício de bits porque o bloco de compactação é sempre um bloco de 4 por 4 texels. As partes não utilizadas do bloco são preenchidas. Embora existam bits desperdiçados nos níveis inferiores, o ganho geral é ainda significativo. Teoricamente, o pior caso é uma textura de 2K por 1 (potência de 2⁰). Aqui, apenas uma única linha de pixels é codificada por bloco, enquanto o restante do bloco é não utilizado.

## <a name="mixing-formats-within-a-single-texture"></a>Misturando formatos dentro de uma única textura

É importante observar que qualquer textura deve especificar que os dados sejam armazenados como 64 ou 128 bits por grupo de 16 texels. Se blocos de 64 bits – ou seja, formatar DXT1 – são usados para a textura, é possível combinar os formatos alfa opaco e de 1 bit por bloco dentro da mesma textura. Em outras palavras, a comparação da magnitude de inteiro sem sinal da cor 0 e da cor 1 é executada exclusivamente para cada bloco de \_ \_ 16 texels.

Depois que os blocos de 128 bits são usados, o canal alfa deve ser especificado no modo explícito (formato DXT2 e DXT3) ou interpolado (formato DXT4 e DXT5) para toda a textura. Assim como acontece com a cor, quando o modo interpolado (formato DXT4 e DXT5) é selecionado, oito alfas interpolados ou seis modos alfas interpolados podem ser usados bloco a bloco. Novamente, a comparação de magnitude de alfa 0 e alfa 1 é feita exclusivamente em uma base \_ \_ bloco a bloco.

O Direct3D fornece serviços para compactar superfícies que são usadas para a texturização de modelos 3D. Esta seção fornece informações sobre como criar e tratar os dados em uma superfície de textura compactada.

As informações estão contidas nos tópicos a seguir.

-   [Texturas alfa opacas e de 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturas com canais alfa (Direct3D 9)](textures-with-alpha-channels.md)
-   [Formatos de textura compactado (Direct3D 9)](compressed-texture-formats.md)
-   [Usando texturas compactadas (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



