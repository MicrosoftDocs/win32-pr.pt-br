---
description: Dicas de otimização do cache de vértice.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Estrutura de D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769372"
---
# <a name="d3ddevinfo_vcache-structure"></a>\_Estrutura D3DDEVINFO VCACHE

Dicas de otimização do cache de vértice.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Padrão**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Padrão de bits. O valor de retorno deve ser o FOURCC (' C', ' A ', ' C', ' H ').

</dd> <dt>

**OptMethod**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Método de otimizações. Use 0 para obter as faixas mais longas. Use 1 para otimizar o uso do cache de vértice.

</dd> <dt>

**CacheSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do cache usado como um destino para otimização. Isso será necessário somente se OptMethod for 1.

</dd> <dt>

**MagicNumber**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Usado por métodos de otimização internos para determinar quando reiniciar as faixas. Isso não pode ser definido ou modificado por um usuário. Isso será necessário somente se OptMethod for 1.

</dd> </dl>

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

 

 
