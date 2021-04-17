---
description: Parâmetros padrão de efeito.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Estrutura D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811519"
---
# <a name="d3dxeffectdefault-structure"></a>Estrutura D3DXEFFECTDEFAULT

Parâmetros padrão de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**pParamName**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome do parâmetro.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

Tipo de dados de uma era. Para obter mais informações, consulte [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**NumBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho, em bytes, dos dados apontados por valores de a.

</dd> <dt>

**Valores**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para o local da memória que contém os dados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
