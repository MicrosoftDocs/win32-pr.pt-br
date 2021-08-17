---
description: Descreve um patch de ordem alta triangular.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c20a846d13cd45bb8a1629fca0e958d3042aacf148c24b0633dd19fb5462bd66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850106"
---
# <a name="d3dtripatch_info-structure"></a>Estrutura D3DTRIPATCH \_ INFO

Descreve um patch de ordem alta triangular.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**StartVertexOffset**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando o deslocamento de vértice, em número de vértices.

</dd> <dt>

**NumVertices**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de vértices.

</dd> <dt>

**Base**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro do tipo [**enumerado D3DBASISTYPE,**](./d3dbasistype.md) que define o tipo de base para o patch de ordem alta triangular. O único valor válido para esse membro é D3DBASIS \_ BEZIER.

</dd> <dt>

**Grau**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro do tipo [**enumerado D3DDEGREETYPE,**](./d3ddegreetype.md) definindo o tipo de grau para o patch de alta ordem triangular.



| Valor                | Número de vértices |
|----------------------|--------------------|
| D3DDEGREE \_ CUBIC     | 10                 |
| D3DDEGREE \_ LINEAR    | 3                  |
| D3DDEGREE \_ QUADTIC | N/D                |
| D3DDEGREE:IC \_   | 21                 |



 

N/A – não disponível. Sem suporte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por exemplo, o diagrama a seguir identifica a ordem do vértice e os números de segmento para um patch de triângulo Bézier cúbica. A ordem do vértice determina os números de segmento usados por [**DrawTriPatch.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) O deslocamento é o número de bytes para o primeiro vértice de patch de triângulo no buffer de vértice.

![diagrama de um patch de ordem alta triangular com nove vértices](images/hop-tripatch-info.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
