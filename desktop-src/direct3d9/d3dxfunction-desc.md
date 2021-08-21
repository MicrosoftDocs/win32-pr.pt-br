---
description: Descreve uma função usada por um efeito .
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: D3DXFUNCTION_DESC (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: fb67f99daa1c0ed551ce989c15e9be2d1f89f8352dfebf7a021ea16f7c69f49e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525653"
---
# <a name="d3dxfunction_desc-structure"></a>Estrutura D3DXFUNCTION \_ DESC

Descreve uma função usada por um efeito .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome da função.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Não utilizado. Esse membro sempre será definido como zero por [**GetFunctionDesc.**](id3dxbaseeffect--getfunctiondesc.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
