---
description: Obtém a semântica para as entradas do sombreador. Use este método para determinar o formato de vértice de entrada.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Função D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771370"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>Função D3DXGetShaderInputSemantics

Obtém a semântica para as entradas do sombreador. Use este método para determinar o formato de vértice de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXGetShaderInputSemantics(
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

Ponteiro para uma matriz de estruturas [**D3DXSEMANTIC**](d3dxsemantic.md) . A função preencherá essa matriz com a semântica para cada elemento de entrada referenciado pelo sombreador. Presume-se que essa matriz contenha pelo menos elementos MAXD3DDECLLENGTH. No entanto, chamar **D3DXGetShaderInputSemantics** com PSemantics = **NULL** retornará o número de elementos necessários para pCount.

</dd> <dt>

*pCount* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Retorna o número de elementos em pSemantics.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use **D3DXGetShaderInputSemantics** para retornar uma lista de semântica de entrada exigida pelo sombreador. Esta é a maneira de descobrir qual é o formato de vértice de entrada para um sombreador de HLSL (linguagem de sombreamento de alto nível). Se o sombreador tiver entradas adicionais que sua declaração de vértice está faltando, você poderá criar um fluxo de vértice extra que tenha um stride de 0 que tenha os componentes ausentes com valores padrão. Por exemplo, essa técnica pode ser usada para fornecer a cor de vértice padrão para modelos que não o especificam.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
