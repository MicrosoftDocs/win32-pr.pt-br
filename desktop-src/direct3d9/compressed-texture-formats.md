---
description: Esta seção contém informações sobre a organização interna de formatos de textura compactada.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formatos de textura compactados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646474"
---
# <a name="compressed-texture-formats-direct3d-9"></a>Formatos de textura compactados (Direct3D 9)

Esta seção contém informações sobre a organização interna de formatos de textura compactada. Você não precisa desses detalhes para usar texturas compactadas, pois você pode usar as funções D3DX para conversão de e para formatos compactados. No entanto, essas informações são úteis se você quiser operar diretamente nos dados da superfície compactada.

O Direct3D usa um formato de compactação que divide mapas de textura em blocos de texel de 4 x 4. Se a textura não tiver transparência - é opaca - ou se a transparência for especificada por um alfa de 1 bit, um bloco de 8 bytes representa o bloco de mapa de textura. Se o mapa da textura contiver texels transparentes, usando um canal alfa, um bloco de 16 bits irá representá-lo.

-   [Texturas opacas e de 1 bit alfa (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturas com canais alfa (Direct3D 9)](textures-with-alpha-channels.md)

Qualquer textura deve especificar que os dados sejam armazenados como 64 ou 128 bits por grupo de 16 texels. Se os blocos de 64 bits-ou seja, o formato DXT1-são usados para a textura, é possível misturar os formatos opaco e de 1 bit alfa em uma base por bloco dentro da mesma textura. Em outras palavras, a comparação da magnitude de inteiro sem sinal da cor \_ 0 e da cor \_ 1 é executada exclusivamente para cada bloco de 16 texels.

Quando blocos de 128 bits são usados, o canal alfa deve ser especificado em um modo explícito (formato DXT2 ou DXT3) ou interpolado (formato DXT4 ou DXT5) para a textura inteira. Da mesma forma que ocorre com a cor, quando o modo interpolado é selecionado, o modo de seis ou oito alfas interpolados pode ser usado em uma base de bloco por bloco. Novamente a comparação de magnitude de alfa \_ 0 e alfa \_ 1 é feita exclusivamente em uma base bloco a bloco.

O Tom dos formatos DXTn é diferente do que foi retornado no DirectX 7,0. A densidade agora é medida em bytes (não blocos). Por exemplo, se você tiver uma largura de 16, terá um timbre de quatro blocos (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de textura compactados](compressed-texture-resources.md)
</dt> </dl>

 

 



