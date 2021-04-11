---
description: Obtém a tabela de sombreador-constante inserida dentro de um sombreador.
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Função D3DXGetShaderConstantTableEx (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2107e7f30733c8f8a19e39e220c4c1d6cb174424
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172999"
---
# <a name="d3dxgetshaderconstanttableex-function"></a>Função D3DXGetShaderConstantTableEx

Obtém a tabela de sombreador-constante inserida dentro de um sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para a função de fluxo DWORD.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Use o \_ sinalizador D3DXCONSTTABLE LARGEADDRESSAWARE para acessar até 4 GB de espaço de endereço virtual (em vez do padrão de 2 GB). Se você não precisar do espaço de endereço virtual adicional, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).

</dd> <dt>

 *ppConstantTable* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retorna a interface da tabela de constantes (consulte [**ID3DXConstantTable**](id3dxconstanttable.md)) que gerencia a tabela de constantes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Uma tabela constante é gerada por [**D3DXCompileShader**](d3dxcompileshader.md) e inserida no corpo do sombreador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
