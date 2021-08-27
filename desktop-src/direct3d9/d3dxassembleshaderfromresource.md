---
description: Função D3DXAssembleShaderFromResource – Montar um sombreador.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Função D3DXAssembleShaderFromResource (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35812be28d847f0c0ced94a05ab9cbcc941f26ef474b7b37ac175e84be263b34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069356"
---
# <a name="d3dxassembleshaderfromresource-function"></a>Função D3DXAssembleShaderFromResource

Montar um sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSrcModule* \[ Em\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Lidar com um módulo que contém a descrição do efeito. Se esse parâmetro for **NULL,** o módulo atual será usado.

</dd> <dt>

*pSrcResource* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do recurso. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*pDefines* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Uma matriz **opcional terminada** em NULL de estruturas [**D3DXMACRO.**](d3dxmacro.md) Esse valor pode ser **NULL.**

</dd> <dt>

*pInclude* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para lidar com \# diretivas de inclusão. Se esse valor for **NULL,** includes serão honorados ao compilar de um arquivo ou causarão um erro quando compilados de um recurso \# ou memória.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Compile opções identificadas por vários sinalizadores. O compilador HLSL do Direct3D 10 agora é o padrão. Consulte [Sinalizadores D3DXSHADER](d3dxshader-flags.md) para obter detalhes.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém o sombreador criado. Esse buffer contém o código do sombreador compilado, bem como qualquer informação de tabela de símbolo e de depuração inserida.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma listagem de erros e avisos que foram encontrados durante a compilação. Essas são as mesmas mensagens que o depurador exibe ao executar no modo de depuração. Esse valor pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXAssembleShaderFromResourceW. Caso contrário, a chamada de função será resolvida para D3DXAssembleShaderFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
