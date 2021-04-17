---
description: Retorna informações de material salvas em arquivos Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Estrutura D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763026"
---
# <a name="d3dxmaterial-structure"></a>Estrutura D3DXMATERIAL

Retorna informações de material salvas em arquivos Direct3D (. x).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>Membros

<dl> <dt>

**MatD3D**
</dt> <dd>

Tipo: **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

Estrutura [**D3DMATERIAL9**](d3dmaterial9.md) que descreve as propriedades do material.

</dd> <dt>

**pTextureFilename**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da textura.

</dd> </dl>

## <a name="remarks"></a>Comentários

As funções [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) e [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) retornam uma matriz de estruturas **D3DXMATERIAL** que especificam a cor do material e o nome da textura para cada material na malha. Em seguida, o aplicativo é necessário para carregar a textura.

O tipo LPD3DXMATERIAL é definido como um ponteiro para a estrutura **D3DXMATERIAL** .


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




