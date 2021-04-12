---
description: A semântica mapeia um parâmetro para os registros de vértice ou de sombreador de pixel. Eles também podem ser cadeias de caracteres descritivas opcionais anexadas a parâmetros que não são de registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Estrutura D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370943"
---
# <a name="d3dxsemantic-structure"></a>Estrutura D3DXSEMANTIC

A semântica mapeia um parâmetro para os registros de vértice ou de sombreador de pixel. Eles também podem ser cadeias de caracteres descritivas opcionais anexadas a parâmetros que não são de registro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opções que identificam como os recursos são usados. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opções que modificam como o uso é interpretado. O índice de uso e uso compõem uma declaração de vértice. Consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A semântica é necessária para os registros de vértice e sombreador de pixel, entrada e saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
