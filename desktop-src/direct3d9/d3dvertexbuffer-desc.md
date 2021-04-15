---
description: Descreve um buffer de vértice.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Estrutura de D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506505"
---
# <a name="d3dvertexbuffer_desc-structure"></a>\_Estrutura desc de D3DVERTEXBUFFER

Descreve um buffer de vértice.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície dos dados do buffer de vértice.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como um buffer de vértice.

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinação de um ou mais sinalizadores [**D3DUSAGE**](d3dusage.md) .

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para este buffer de vértice.

</dd> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do buffer de vértice, em bytes.

</dd> <dt>

**FVF**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinação de [D3DFVF](d3dfvf.md) que descreve o formato de vértice dos vértices nesse buffer.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[Buffers de vértice (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
