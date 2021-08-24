---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb7a22570e92945df8ab599f8c95bdffa1d03dd9ac83e35dfc7bb849bd42d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853326"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Um buffer somente leitura que é indexado em bytes.



| Método                                                              | Descrição                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Obtém as dimensões do recurso. |
| [**Carregar**](byteaddressbuffer-load.md)                              | Obtém um valor.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Obtém dois valores.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Obtém três valores.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Obtém quatro valores.             |



 

Você pode usar o **tipo de objeto ByteAddressBuffer** ao trabalhar com buffers brutos. Para obter mais informações sobre a exibição bruta de buffers, consulte [Exibições brutas de buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esse objeto tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Com suporte |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Modelo de sombreador [5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior Modelo [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10.0 ou 10.1 ([**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 X) em dispositivos que suportam sombreadores \_ de computação. Para obter mais informações sobre o suporte ao sombreador de computação em hardware de nível baixo, consulte [Sombreadores](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)de computação no hardware de nível baixo .)<br/> | sim       |



 

Esse objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Para obter mais informações sobre um buffer de endereço de byte, consulte o [tipo de recurso acessível por byte](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

O Modelo 5 do Sombreador também implementa um buffer [de endereço de byte de leitura/gravação.](sm5-object-rwbyteaddressbuffer.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Modelo de Sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

