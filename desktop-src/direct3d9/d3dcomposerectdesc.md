---
description: Especifica o retângulo usado para incluir glifos em uma superfície monocromática.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Estrutura D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8c23868e8759b98898013ea70d8d62768f1e648eb6e5019eb52dd21ba55905b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733199"
---
# <a name="d3dcomposerectdesc-structure"></a>Estrutura D3DCOMPOSERECTDESC

Especifica o retângulo usado para incluir glifos em uma superfície monocromática.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>Membros

<dl> <dt>

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

</dd> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de texels da coordenada esquerda.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de texels da coordenada superior.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada em chamadas para [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para incluir glifos na superfície de origem. Um buffer de vértice (consulte [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) preenchido com essas estruturas é criado para conter os locais de glifo. Os membros USHORT são usados para reduzir o volume de memória o máximo possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
