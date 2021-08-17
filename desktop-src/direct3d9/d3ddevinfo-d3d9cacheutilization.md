---
description: Mede o desempenho da taxa de acertos do cache para texturas e vértices indexados.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 01f0521ca7833cd74c3cb45b5a650fbd12aae485e36a153b57e6d9b10b49d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733067"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>Estrutura D3DDEVINFO \_ D3D9CACHEUTILIZATION

Mede o desempenho da taxa de acertos do cache para texturas e vértices indexados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**TextureCacheHitRate**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa de acertos para localizar uma textura no cache de textura. Isso pressu que haja um cache de textura. Aumentar o desvio de nível de detalhes para usar a textura mais detalhada, usar muitas texturas grandes ou produzir um padrão de acesso de textura quase aleatório em texturas grandes com código de sombreador personalizado pode afetar drasticamente a taxa de acertos do cache de textura.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa de acertos para localizar vértices transformados no cache de vértice. A GPU foi projetada para transformar vértices indexados e pode armazená-los em um cache de vértice. Se você estiver usando malhas, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) ou [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) poderá resultar em uma melhor utilização do cache de vértice.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um cache eficiente normalmente é mais próximo de uma taxa de acertos de 90%, e um cache ineficiente normalmente está mais próximo de uma taxa de acertos de 10% (embora um percentual baixo não seja necessariamente um problema).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
