---
description: Parâmetros padrão de efeito.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Estrutura D3DXEFFECTDEFAULT (D3dx9mesh.h)
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
ms.openlocfilehash: 41beda43807ace6b0f335dc1937f8843cbc11544e4842f86af98eb0e0bb0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731875"
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

Tipo de dados em pValue. Para obter mais informações, [ **consulte D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**NumBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho, em bytes, dos dados apontados por pValue.

</dd> <dt>

**Pvalue**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ponteiro para o local de memória que contém os dados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
