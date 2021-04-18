---
description: Os valores de largura, altura e profundidade da estrutura de D3D12_DISPATCH_RAYS_DESC especificada na chamada DispatchRays de origem.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760627"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

A largura, a altura e os valores de profundidade da estrutura desc de raios de expedição de D3D12 especificadas na chamada de [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) de origem. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador resgatável**](callable-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)

## <a name="see-also"></a>Confira também

* [Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
