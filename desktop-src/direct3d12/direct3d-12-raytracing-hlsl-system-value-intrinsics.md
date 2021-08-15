---
title: Intrínsecos de valor do sistema HLSL de raytracing do Direct3D 12
description: Veja links para artigos que descrevem funções intrínsecas de valor do sistema HLSL (linguagem de sombreador de alto nível) que suportam o pipeline de raytracing do Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b2a2cbd870da41df94ee0389757a1d1ec7cd5e4549a3abd32dbaaf6a7c8e8e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045554"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Intrínsecos de valor do sistema HLSL de raytracing do Direct3D 12

Os valores do sistema são recuperados usando funções intrínsecas especiais, em vez de incluir parâmetros com semântica especial na assinatura da função do sombreador. 

## <a name="in-this-section"></a>Nesta seção

### <a name="ray-dispatch-system-values"></a>Valores do sistema de expedição de raios

| Tópico | Descrição |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Obtém o local atual x e y dentro da largura e altura obtidas com o valor intrínseco do sistema **DispatchRaysDimensions.** |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Os valores de largura, altura e profundidade da estrutura **D3D12 \_ \_ DISPATCH RAY \_ DESC** especificada na chamada **DispatchRays** de origem. |

### <a name="ray-system-values"></a>Valores do sistema de raios

| Tópico | Descrição |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | A origem do espaço do mundo do raio atual. |
| [**WorldRayDirection**](worldraydirection.md) | A direção do espaço do mundo para o raio atual. |
| [**RayTMin**](raytmin.md) | Um float que representa o ponto de partida paramétrico atual para o raio. |
| [**RayTCurrent**](raytcurrent.md) | Um float que representa o ponto final paramétrico atual para o raio.  |
| [**RayFlags**](rayflags.md) | Um inteiro sem sinal que contém os sinalizadores **ray_flag** dados atuais. |

### <a name="primitiveobject-space-system-values"></a>Valores do sistema de espaço primitivo/objeto

| Tópico | Descrição |
|-|-|
| [**InstanceIndex**](instanceindex.md) | O índice gerado automaticamente da instância atual na estrutura de aceleração de raio de nível superior. |
| [**Instanceid**](instanceid.md) | O identificador fornecido pelo usuário para a instância na instância da estrutura de aceleração de nível inferior dentro da estrutura de nível superior. |
| [**PrimitiveIndex**](primitiveindex.md) | O índice gerado automaticamente do primitivo dentro da geometria dentro da instância da estrutura de aceleração de nível inferior. |
| [**ObjectRayOrigin**](objectrayorigin.md) | A origem do espaço do objeto para o raio atual. |
| [**ObjectRayDirection**](objectraydirection.md) | A direção do espaço do objeto para o raio atual. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Uma matriz para transformar do espaço do objeto para o espaço do mundo. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Uma matriz para transformar do espaço do objeto para o espaço do mundo. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Uma matriz para transformar do espaço do mundo para o espaço do objeto |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Uma matriz para transformar do espaço do mundo para o espaço do objeto |
### <a name="hit-specific-system-values"></a>Valores do sistema específicos a um acerto

| Tópico | Descrição |
|-|-|
| [**HitKind**](hitkind.md) | Retorna o valor passado como o **parâmetro HitKind** para [**ReportHit**](reporthit-function.md). |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência principal](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
