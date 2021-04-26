---
title: Objetos do Shader Model 5,1
description: Os seguintes objetos foram adicionados ao modelo do sombreador 5,1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c56fbe035f63bd8f25a8b34377c333c2ce9946c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993853"
---
# <a name="shader-model-51-objects"></a>Objetos do Shader Model 5,1

Os seguintes objetos foram adicionados ao modelo do sombreador 5,1.

Para as [exibições de ordem de rasterizador](/windows/desktop/direct3d11/rasterizer-order-views) (disponíveis no D3D 11.3 e D3D12), os seguintes objetos são novos e são permitidos somente no sombreador de pixel. Observe que os métodos aos quais eles dão suporte são idênticos aos objetos UAV correspondentes.



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| Objeto rasterizador                  | Objeto UAV                                                    |
| RasterizerOrderedBuffer            | [**RWBuffer**](sm5-object-rwbuffer.md)                       |
| RasterizerOrderedByteAddressBuffer | [**RWByteAddressBuffer**](sm5-object-rwbyteaddressbuffer.md) |
| RasterizerOrderedStructuredBuffer  | [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo do sombreador 5,1](shader-model-5-1.md)
</dt> <dt>

[Recursos do HLSL Shader Model 5,1 para Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
