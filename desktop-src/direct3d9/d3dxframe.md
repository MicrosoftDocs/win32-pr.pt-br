---
description: Encapsula um quadro de transformação em uma hierarquia de quadros de transformação.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Estrutura D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173002"
---
# <a name="d3dxframe-structure"></a>Estrutura D3DXFRAME

Encapsula um quadro de transformação em uma hierarquia de quadros de transformação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome do quadro.

</dd> <dt>

**TransformationMatrix**
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

Matriz de transformação.

</dd> <dt>

**pMeshContainer**
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

Ponteiro para o contêiner de malha.

</dd> <dt>

**pFrameSibling**
</dt> <dd>

Tipo: * * * * D3DXFRAME **\***

</dd> <dd>

Ponteiro para um quadro irmão.

</dd> <dt>

**pFrameFirstChild**
</dt> <dd>

Tipo: * * * * D3DXFRAME **\***

</dd> <dd>

Ponteiro para um quadro filho.

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

 

 




