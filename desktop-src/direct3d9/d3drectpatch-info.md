---
description: Descreve um patch de ordem superior retangular.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Estrutura de D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761257"
---
# <a name="d3drectpatch_info-structure"></a>Estrutura de informações do D3DRECTPATCH \_

Descreve um patch de ordem superior retangular.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**StartVertexOffsetWidth**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando a largura de deslocamento do vértice, em número de vértices.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando a altura de deslocamento do vértice, em número de vértices.

</dd> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura de cada vértice, em número de vértices.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura de cada vértice, em número de vértices.

</dd> <dt>

**Passo**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura da matriz de vértices imaginários bidimensionais, que ocupa o mesmo espaço que o buffer de vértice. Para obter um exemplo, consulte o diagrama a seguir.

</dd> <dt>

**Base**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , definindo o tipo base para o patch de ordem superior retangular.



| Valor                 | Pedido com suporte            | Largura e altura                  |
|-----------------------|----------------------------|-----------------------------------|
| \_BEZIER D3DBASIS      | Linear, cúbica e QUINTIC | Width = altura = (DWORD) ordem + 1 |
| D3DBASIS \_ BSPLINE     | Linear, cúbica e QUINTIC | Largura = altura > (DWORD) ordem  |
| \_Interpolação de D3DBASIS | Baias                      | Largura = altura > (DWORD) ordem  |



 

</dd> <dt>

**Grau**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , definindo o grau para o patch retangular.

</dd> </dl>

## <a name="remarks"></a>Comentários

O diagrama a seguir identifica os parâmetros que especificam um patch de retângulo.

![diagrama de um patch de ordem superior retangular e os parâmetros que o especificam](images/hop-rectpatch.png)

Cada um dos vértices no buffer de vértice é mostrado como um ponto preto. Nesse caso, o buffer de vértice tem 20 vértices, 16 dos quais estão no patch de retângulo. O stride é o número de vértices na largura do buffer de vértice, neste caso, cinco. O deslocamento x para o primeiro vértice é chamado de StartIndexVertexWidth e, nesse caso, 1. O deslocamento y para o primeiro vértice do patch é chamado de StartIndexVertexHeight e, nesse caso, 0.

Para renderizar um fluxo de patches retangulares individuais (não-mosaico), você deve interpretar a geometria como um patch retangular longo estreito (1 x N). A estrutura de **\_ informações de D3DRECTPATCH** para tal faixa (Bézier cúbica) seria configurada da seguinte maneira.


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
