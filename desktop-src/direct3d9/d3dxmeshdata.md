---
description: Estrutura de dados de malha.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: Estrutura D3DXMESHDATA (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298484"
---
# <a name="d3dxmeshdata-structure"></a>Estrutura D3DXMESHDATA

Estrutura de dados de malha.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**

</dd> <dd>

Define o tipo de dados de malha. Consulte [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).

</dd> <dt>

**pMesh**
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

</dd> <dd>

Ponteiro para uma malha. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

**pPatchMesh**
</dt> <dd>

Tipo: **LPD3DXPATCHMESH**

</dd> <dd>

Ponteiro para uma malha de patch. Consulte [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)
</dt> </dl>

 

 
