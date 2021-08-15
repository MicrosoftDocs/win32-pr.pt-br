---
description: Define uma cor de material básica que pode ser aplicada a uma malha completa ou a rostos individuais de uma malha. A potência é o expoente especular do material.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4dcb1cef7597ff7c02d16f1db311287511166c9259c89a0ea60a0c49fb7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798963"
---
# <a name="material"></a>Material

Define uma cor de material básica que pode ser aplicada a uma malha completa ou a rostos individuais de uma malha. A potência é o expoente especular do material.

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

-   faceColor – cor da face. Um modelo ColorRGBA. Consulte [**ColorRGBA**](colorrgba.md).
-   power – expoente de cor especular de material.
-   specularColor – cor especular do material. Um modelo ColorRGB. Consulte [**ColorRGB**](colorrgb.md).
-   emissiveColor – cor emissiva do material. Um modelo ColorRGB. Consulte [**ColorRGB**](colorrgb.md).

> [!Note]  
> A cor do ambiente requer um componente alfa.

 

[**TextureFilename é**](texturefilename.md) um objeto de dados opcional. Se esse objeto não estiver presente, o rosto será sem texto.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



