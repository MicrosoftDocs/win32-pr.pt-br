---
description: Descreve um patch de ordem superior triangular.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Estrutura de D3DTRIPATCH_INFO (D3D9Types. h)
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
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780303"
---
# <a name="d3dtripatch_info-structure"></a>Estrutura de informações do D3DTRIPATCH \_

Descreve um patch de ordem superior triangular.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando deslocamento de vértice, em número de vértices.

</dd> <dt>

**NumVertices**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de vértices.

</dd> <dt>

**Base**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , que define o tipo base para o patch de ordem superior triangular. O único valor válido para esse membro é D3DBASIS \_ BEZIER.

</dd> <dt>

**Grau**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , definindo o tipo de grau para o patch de ordem superior triangular.



| Valor                | Número de vértices |
|----------------------|--------------------|
| D3DDEGREE \_ cúbico     | 10                 |
| D3DDEGREE \_ linear    | 3                  |
| D3DDEGREE \_ quadrática | N/D                |
| D3DDEGREE \_ QUINTIC   | 21                 |



 

N/A-não disponível. Não há suporte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por exemplo, o diagrama a seguir identifica a ordem de vértice e os números de segmento para um patch de triângulo Bézier cúbico. A ordem de vértice determina os números de segmento usados pelo [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch). O deslocamento é o número de bytes para o primeiro vértice de patch de triângulo no buffer de vértice.

![diagrama de um patch de ordem superior triangular com nove vértices](images/hop-tripatch-info.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
