---
title: ConsumeStructuredBuffer
description: Um buffer de entrada que aparece como um fluxo do qual o sombreador pode receber valores. Somente os buffers estruturados podem usar tipos T que são estruturas.
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
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988712"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Um buffer de entrada que aparece como um fluxo do qual o sombreador pode receber valores. Somente os buffers estruturados podem usar tipos T que são estruturas.



| Método                                                                    | Descrição                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Consumir**](sm5-object-consumestructuredbuffer-consume.md)             | Remove um valor do final do buffer. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Obtém as dimensões do recurso.               |



 

O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .

O UAV associado a esse recurso deve ter sido criado com o [**D3D11 \_ buffer \_ UAV \_ sinalizador \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Para obter mais informações sobre o consumo de buffers estruturados, consulte as duas seções: [acrescentar e consumir](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer e [buffer estruturado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 