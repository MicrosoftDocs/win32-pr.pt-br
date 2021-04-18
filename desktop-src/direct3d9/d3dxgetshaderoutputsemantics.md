---
description: Obtenha a semântica para todos os elementos de saída do sombreador.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Função D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506477"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a>Função D3DXGetShaderOutputSemantics

Obtenha a semântica para todos os elementos de saída do sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para o fluxo DWORD da função de sombreador.

</dd> <dt>

*pSemantics* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Ponteiro para uma matriz de estruturas [**D3DXSEMANTIC**](d3dxsemantic.md) . A função preencherá essa matriz com a semântica para cada elemento de saída referenciado pelo sombreador. Presume-se que essa matriz contenha pelo menos elementos MAXD3DDECLLENGTH. No entanto, chamar **D3DXGetShaderOutputSemantics** com PSemantics = **NULL** retornará o número de elementos necessários para pCount.

</dd> <dt>

*pCount* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Retorna o número de elementos em pSemantics.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
