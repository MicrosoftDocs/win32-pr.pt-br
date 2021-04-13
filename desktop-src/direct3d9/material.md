---
description: Define uma cor de material básica que pode ser aplicada a uma malha completa ou a faces individuais de uma malha. A potência é o expoente especular do material.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456370"
---
# <a name="material"></a>Material

Define uma cor de material básica que pode ser aplicada a uma malha completa ou a faces individuais de uma malha. A potência é o expoente especular do material.

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

Em que:

-   faceColor-face de cor. Um modelo ColorRGBA. Consulte [**ColorRGBA**](colorrgba.md).
-   expoente de cor do especular de material de energia.
-   specularColor-cor especular de material. Um modelo ColorRGB. Consulte [**colorRGB**](colorrgb.md).
-   emissiveColor-material emissiva Color. Um modelo ColorRGB. Consulte [**colorRGB**](colorrgb.md).

> [!Note]  
> A cor do ambiente requer um componente alfa.

 

[**TextureFilename**](texturefilename.md) é um objeto de dados opcional. Se esse objeto não estiver presente, a face não será texturizada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



