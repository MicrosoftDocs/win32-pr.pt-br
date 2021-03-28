---
title: RWStructuredBuffer
description: Um buffer de leitura/gravação que pode usar um tipo T que é uma estrutura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366194"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Um buffer de leitura/gravação que pode usar um tipo T que é uma estrutura.



| Método                                                                     | Descrição                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Decrementa o contador oculto do objeto. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Obtém as dimensões do recurso.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Incrementa o contador oculto do objeto. |
| [**Carregamento**](rwstructuredbuffer-load.md)                                    | Lê dados de buffer.                      |
| [**Operador\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Retorna uma variável de recurso.            |



 

Uma variável de recurso também pode ser passada para qualquer operação não ordenada ou interbloqueada.

Os objetos RWStructuredBuffer podem ser prefixados com a classe de armazenamento **globallycoherent**. Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização só liberará um UAV dentro do grupo atual.

O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .

Para saber mais sobre [buffers estruturados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte o material de visão geral.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Com suporte |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10,0 ou 10,1 ([**\_ \_ nível**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)de recurso do D3D \_ 10 \_ X) em dispositivos que dão suporte a sombreadores de computação. Para obter mais informações sobre o suporte de sombreador de computação em hardware de nível inferior, consulte [sombreadores de computação em hardware de nível inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

