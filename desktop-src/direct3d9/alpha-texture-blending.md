---
description: O mecanismo de iluminação combina a cor do material, a cor do vértice e as informações de iluminação para gerar uma cor por vértice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Mesclagem de textura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812868"
---
# <a name="alpha-texture-blending-direct3d-9"></a>Mesclagem de textura alfa (Direct3D 9)

O mecanismo de iluminação combina a cor do material, a cor do vértice e as informações de iluminação para gerar uma cor por vértice. Depois de interpolado, isso gera uma cor por pixel que é gravada no buffer de quadro. Se um aplicativo habilitar a mesclagem de textura, a cor do pixel se tornará uma combinação do pixel atual no buffer do quadro e uma cor de textura.

Esta fórmula determina a cor do pixel misturado final:


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



Em que:

-   Color é a cor do pixel de saída.
-   TexelColor é a cor de entrada após a filtragem de textura.
-   SourceBlend é a porcentagem da cor de pixel final que é composta pela cor de Texel de origem.
-   CurrentPixelColor é a cor do pixel atual.
-   DestBlend é a porcentagem da cor final do pixel que é composta pela cor atual do pixel.

A equação de mesclagem final é definida chamando [**IDirect3DDevice9:: Setrenderingstate**](/windows/desktop/api) e especificando o estado de renderização de Blend (D3DRS \_ BLENDXXX) com um fator de mistura correspondente ([**D3DBLEND**](./d3dblend.md)). Os valores de SourceBlend e DestBlend variam de 0,0 (transparente) a 1,0 (opaco) inclusive. Além disso, um aplicativo pode controlar a transparência de um pixel definindo o valor alfa em uma textura. Nesse caso, use o seguinte:


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



A equação de mesclagem fará com que o pixel renderizado seja transparente. Os valores padrão são:


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de textura](texture-blending.md)
</dt> <dt>

[Filtragem de textura (Direct3D 9)](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
