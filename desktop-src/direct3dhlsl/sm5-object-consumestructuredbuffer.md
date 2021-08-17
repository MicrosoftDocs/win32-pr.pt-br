---
title: ConsumeStructuredBuffer
description: Um buffer de entrada que aparece como um fluxo do qual o sombreador pode efetuar pull de valores. Somente buffers estruturados podem usar tipos T que são estruturas.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4e0530c98b78f9b18b0934874fb5a082779694ced2f171293d0a38dc458a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986086"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Um buffer de entrada que aparece como um fluxo do qual o sombreador pode efetuar pull de valores. Somente buffers estruturados podem usar tipos T que são estruturas.



| Método                                                                    | Descrição                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Consumir**](sm5-object-consumestructuredbuffer-consume.md)             | Remove um valor do final do buffer. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Obtém as dimensões do recurso.               |



 

O formato UAV vinculado a esse recurso precisa ser criado com o formato DXGI \_ FORMAT \_ UNKNOWN.

O UAV vinculado a esse recurso deve ter sido criado com [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Para obter mais informações sobre como consumir buffers estruturados, consulte ambas as seções: [anexar](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e consumir buffer e [buffer estruturado.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esse objeto tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Esse objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Modelo de Sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 