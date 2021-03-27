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
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967219"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Um buffer somente leitura que é indexado em bytes.



| Método                                                              | Descrição                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Obtém as dimensões do recurso. |
| [**Carregamento**](byteaddressbuffer-load.md)                              | Obtém um valor.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Obtém dois valores.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Obtém três valores.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Obtém quatro valores.             |



 

Você pode usar o tipo de objeto **ByteAddressBuffer** ao trabalhar com buffers brutos. Para obter mais informações sobre a exibição bruta de buffers, consulte [exibições brutas de buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Com suporte |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10,0 ou 10,1 ([**\_ \_ nível**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)de recurso do D3D \_ 10 \_ X) em dispositivos que dão suporte a sombreadores de computação. Para obter mais informações sobre o suporte de sombreador de computação em hardware de nível inferior, consulte [sombreadores de computação em hardware de nível inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Para obter mais informações sobre um buffer de endereço de byte, consulte o [tipo de recurso de byte endereçável](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

O Shader Model 5 também implementa um [buffer de endereço de byte de leitura/gravação](sm5-object-rwbyteaddressbuffer.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

