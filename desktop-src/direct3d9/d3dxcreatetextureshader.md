---
description: Cria um objeto de sombreador de textura do sombreador compilado.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: Função D3DXCreateTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298630"
---
# <a name="d3dxcreatetextureshader-function"></a>Função D3DXCreateTextureShader

Cria um objeto de sombreador de textura do sombreador compilado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para a função de fluxo DWORD.

</dd> <dt>

*ppTextureShader* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***

Retorna um objeto [**ID3DXTextureShader**](id3dxtextureshader.md) que pode ser usado para preencher de procedimento o conteúdo de uma textura usando as funções [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .

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

 

 
