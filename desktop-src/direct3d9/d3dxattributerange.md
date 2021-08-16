---
description: Estrutura D3DXATTRIBUTERANGE – armazena uma entrada de tabela de atributo.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Estrutura D3DXATTRIBUTERANGE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 73fe2214b2c1b8acb1bc657bd41803c425b4c86f34d022d6367c3011eebd6d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526804"
---
# <a name="d3dxattributerange-structure"></a>Estrutura D3DXATTRIBUTERANGE

Armazena uma entrada de tabela de atributo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Atribid**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de tabela de atributo.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando face.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem de face.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando vértice.

</dd> <dt>

**Contagemdevértice**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem de vértices.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante. Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.

O tipo LPD3DXATTRIBUTERANGE é definido como um ponteiro para a estrutura **D3DXATTRIBUTERANGE** .


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
