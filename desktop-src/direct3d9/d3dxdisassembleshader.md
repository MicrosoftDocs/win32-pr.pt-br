---
description: Desmontar um sombreador.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Função D3DXDisassembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781621"
---
# <a name="d3dxdisassembleshader-function"></a>Função D3DXDisassembleShader

Desmontar um sombreador.

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você use a API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pShader* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para um buffer de memória que contém os dados do sombreador.

</dd> <dt>

*EnableColorCode* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Habilite o código de cor para facilitar a leitura da desmontagem.

</dd> <dt>

*pComments* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres de comentário opcional com terminação nula. Esse valor pode ser **nulo**.

</dd> <dt>

*ppDisassembly* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém o sombreador desmontado. Consulte [**ID3DXBuffer**](id3dxbuffer.md).

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

 

 
