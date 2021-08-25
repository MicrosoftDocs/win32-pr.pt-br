---
description: Define as operações a executar em vértices na preparação para limpeza de malha.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumeração D3DXCLEANTYPE (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 2517c59d5505a8f2892ef0aee1d3884b8d489625637002d6e69a4f86434237fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894106"
---
# <a name="d3dxcleantype-enumeration"></a>Enumeração D3DXCLEANTYPE

Define as operações a executar em vértices na preparação para limpeza de malha.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKFACING**
</dt> <dd>

Triângulos de mesclagem que compartilham os mesmos índices de vértice, mas têm normais de face apontando em direções opostas (triângulos voltados para trás). A menos que os triângulos não sejam divididos adicionando um vértice replicado, os dados de adjacency de malha dos dois triângulos poderão estar em conflito.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ CURVETIES**
</dt> <dd>

Se um vértice for o ápice de dois ventiladores de triângulo (um arco) e as operações de malha afetarem um dos ventiladores, divida o vértice compartilhado em dois novos vértices. Os arcos podem causar problemas para operações como simplificação de malha que removem vértices, pois a remoção de um vértice afeta dois conjuntos distintos de triângulos.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ SKINNING**
</dt> <dd>

Use esse sinalizador para evitar loops infinitos durante operações de malha de instalação de montagem.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**OTIMIZAÇÃO D3DXCLEAN \_**
</dt> <dd>

Use esse sinalizador para evitar loops infinitos durante operações de otimização de malha.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**SIMPLIFICAÇÃO D3DXCLEAN \_**
</dt> <dd>

Use esse sinalizador para evitar loops infinitos durante operações de simplificação de malha.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




