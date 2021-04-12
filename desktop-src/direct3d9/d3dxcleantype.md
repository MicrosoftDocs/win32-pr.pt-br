---
description: Define operações a serem executadas em vértices em preparação para limpeza de malha.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumeração D3DXCLEANTYPE (D3dx9mesh. h)
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
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173045"
---
# <a name="d3dxcleantype-enumeration"></a>Enumeração D3DXCLEANTYPE

Define operações a serem executadas em vértices em preparação para limpeza de malha.

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

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**\_Volta D3DXCLEAN**
</dt> <dd>

Mescle triângulos que compartilham os mesmos índices de vértice, mas que têm normalidades de face apontando para direções opostas (triângulos voltados para o verso). A menos que os triângulos não sejam divididos adicionando um vértice replicado, os dados de adjacência da malha dos dois triângulos podem entrar em conflito.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**
</dt> <dd>

Se um vértice for o Apex de dois fãs de triângulo (um bowtie) e operações de malha afetarão um dos ventiladores, dividirá o vértice compartilhado em dois novos vértices. O bowties pode causar problemas para operações como a simplificação da malha que Remove vértices, porque a remoção de um vértice afeta dois conjuntos distintos de triângulos.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN de \_ aparência**
</dt> <dd>

Use esse sinalizador para evitar loops infinitos durante as operações de malha da configuração de revestimento.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**Otimização de D3DXCLEAN \_**
</dt> <dd>

Use esse sinalizador para evitar loops infinitos durante operações de otimização de malha.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Simplificação de D3DXCLEAN**
</dt> <dd>

Use esse sinalizador para evitar loops infinitos durante operações de simplificação de malha.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




