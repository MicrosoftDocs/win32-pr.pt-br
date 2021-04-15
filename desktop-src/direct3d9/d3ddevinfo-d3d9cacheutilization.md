---
description: Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Estrutura de D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
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
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506465"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>\_Estrutura D3DDEVINFO D3D9CACHEUTILIZATION

Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa de sucesso para localizar uma textura no cache de textura. Isso pressupõe que haja um cache de textura. Aumentar a tendência de nível de detalhe para usar a textura mais detalhada, usar muitas texturas grandes ou produzir um padrão de acesso de textura quase aleatória em texturas grandes com código de sombreador personalizado pode afetar drasticamente a taxa de sucesso do cache de textura.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

A taxa de sucesso para localizar vértices transformados no cache de vértice. A GPU é projetada para transformar vértices indexados e pode armazená-los em um cache de vértice. Se você estiver usando malhas, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) ou [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) poderá resultar em melhor utilização de cache de vértice.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um cache eficiente é geralmente mais próximo de uma taxa de impacto de 90% e um cache ineficiente geralmente é mais próximo de uma taxa de impacto de 10% (embora uma porcentagem baixa não seja necessariamente um problema).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
