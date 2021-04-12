---
description: Encapsula um objeto de malha em uma hierarquia de quadros de transformação.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Estrutura D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298485"
---
# <a name="d3dxmeshcontainer-structure"></a>Estrutura D3DXMESHCONTAINER

Encapsula um objeto de malha em uma hierarquia de quadros de transformação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome da malha.

</dd> <dt>

**MeshData**
</dt> <dd>

Tipo: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Tipo de dados na malha. Consulte [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**pMaterials**
</dt> <dd>

Tipo: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Matriz de materiais de malha. Consulte [**D3DXMATERIAL**](d3dxmaterial.md).

</dd> <dt>

**pEffects**
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Ponteiro para um conjunto de parâmetros de efeito padrão. Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**NumMaterials**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de materiais na malha.

</dd> <dt>

**pAdjacency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Ponteiro para uma matriz de três DWORDs por triângulo da malha que contém informações de adjacência.

</dd> <dt>

**pSkinInfo**
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Ponteiro para a interface de informações da capa. Consulte [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**pNextMeshContainer**
</dt> <dd>

Tipo: * * * * D3DXMESHCONTAINER **\***

</dd> <dd>

Ponteiro para o próximo contêiner de malha.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo pode derivar dessa estrutura para adicionar outros dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
