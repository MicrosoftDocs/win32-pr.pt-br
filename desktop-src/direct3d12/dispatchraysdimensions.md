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
ms.openlocfilehash: 4f68b7bdd5f5ea92074b366b9f981f490a9801079b29def17ba66770abd3c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989486"
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
