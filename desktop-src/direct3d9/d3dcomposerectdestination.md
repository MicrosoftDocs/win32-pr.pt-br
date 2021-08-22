---
description: Especifica o glifo de origem e o local em uma superfície monocromática para a cópia de glifos.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Estrutura D3DCOMPOSERECTDESTINATION (D3d9types.h)
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
ms.openlocfilehash: e6d859cb0bfd47c9be21f37feef287b38cdce4cc64360dd312b2b52bb825a23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123306"
---
# <a name="d3dcomposerectdestination-structure"></a>Estrutura D3DCOMPOSERECTDESTINATION

Especifica o glifo de origem e o local em uma superfície monocromática para a cópia de glifos.

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

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Indexe o glifo específico do buffer de vértice que [**contém estruturas D3DCOMPOSERECTDESC.**](d3dcomposerectdesc.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Reservado para fins de alinhamento.

</dd> <dt>

**X**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada esquerda em que começar a copiar.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada superior em que começar a copiar.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada em chamadas para [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) para indicar que os glifos de local devem ser copiados e para qual glifo específico deve ser copiado. Um buffer de vértice (consulte [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) preenchido com essas estruturas é criado para conter os locais de glifo. Os membros USHORT são usados para reduzir o espaço de memória tanto quanto possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
