---
description: O tipo de objeto.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: D3DXPARAMETER_CLASS enumeração (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 10d786dbbb50c44519f4f6bb1239b9fd07dfadeb706c13eca588051a918103cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525235"
---
# <a name="d3dxparameter_class-enumeration"></a>Enumeração D3DXPARAMETER \_ CLASS

O tipo de objeto.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**ESCALAR D3DXPC \_**
</dt> <dd>

Constante é um escalar.

</dd> <dt>

<span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**VETOR D3DXPC \_**
</dt> <dd>

Constante é um vetor.

</dd> <dt>

<span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**LINHAS DE MATRIZ D3DXPC \_ \_**
</dt> <dd>

Constante é uma matriz principal de linha.

</dd> <dt>

<span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**COLUNAS DE MATRIZ D3DXPC \_ \_**
</dt> <dd>

Constante é uma matriz principal de coluna.

</dd> <dt>

<span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**OBJETO D3DXPC \_**
</dt> <dd>

Constante é uma textura, sombreador ou uma cadeia de caracteres.

</dd> <dt>

<span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC \_ STRUCT**
</dt> <dd>

Constante é uma estrutura.

</dd> <dt>

<span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




