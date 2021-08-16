---
description: Define sinalizadores usados para controlar o número ou matrizes que o sistema aplica ao executar a combinação de vértices multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumeração D3DVERTEXBLENDFLAGS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecc7f99e26088ff03b626604279bffe5c64ddb82b95a6f6219b637b3fce5a59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527300"
---
# <a name="d3dvertexblendflags-enumeration"></a>Enumeração D3DVERTEXBLENDFLAGS

Define sinalizadores usados para controlar o número ou matrizes que o sistema aplica ao executar a combinação de vértices multimatrix.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ DISABLE**
</dt> <dd>

Desabilitar a combinação de vértices; aplicar somente a matriz mundial definida pela macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) em que o valor do índice para o estado de transformação é 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Habilita a mesclagem de vértice entre as duas matrizes definidas pela macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) em que o valor do índice para os estados de transformação é 0 e 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Habilita a mesclagem de vértice entre as três matrizes definidas pela macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) em que o valor do índice para os estados de transformação é 0, 1 e 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Habilita a combinação de vértices entre as quatro matrizes definidas pela macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) em que o valor do índice para os estados de transformação é 0, 1, 2 e 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF \_ TWEENING**
</dt> <dd>

A combinação de vértices é feita usando o valor atribuído a D3DRS \_ TWEENFACTOR.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Use uma única matriz com um peso de 1,0.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros desse tipo são usados com o estado de \_ renderização VERTEXBLEND D3DRS.

A mesclagem de geometria (mesclagem de vértice multimatrix) requer que seu aplicativo use um formato de vértice que tenha pesos de mesclagem (beta) para cada vértice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ WORLD**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
