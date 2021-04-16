---
description: Especifica o glifo de origem e o local em uma superfície monocromática para copiar glifos.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Estrutura D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768371"
---
# <a name="d3dcomposerectdestination-structure"></a>Estrutura D3DCOMPOSERECTDESTINATION

Especifica o glifo de origem e o local em uma superfície monocromática para copiar glifos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**SrcRectIndex**
</dt> <dd>

Tipo: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Um glifo específico de índice do buffer de vértices que contém estruturas [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Reservado para fins de alinhamento.

</dd> <dt>

**X**
</dt> <dd>

Tipo: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada esquerda para iniciar a cópia em.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada superior para iniciar a cópia em.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada em chamadas para [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para indicar que os glifos de local devem ser copiados para e qual glifo específico deve ser copiado. Um buffer de vértice (consulte [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) preenchido com essas estruturas é criado para conter os locais de glifo. Os membros USHORT são usados para reduzir o volume de memória o máximo possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
