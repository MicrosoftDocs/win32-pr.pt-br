---
description: Pré-processa um arquivo de sombreador sem executar a compilação. Isso resolve tudo o que define e inclui, fornecendo um sombreador \# \# autossunte para compilação subsequente.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: Função D3DXPreprocessShaderFromFile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f254e3a06138b23b33775e1434346e73b8fde51d4c65e4ff368c11ab4521bb46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044734"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a>Função D3DXPreprocessShaderFromFile

Pré-processa um arquivo de sombreador sem executar a compilação. Isso resolve tudo o que define e inclui, fornecendo um sombreador \# \# autossunte para compilação subsequente.

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess)

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo do sombreador.

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

*ppShaderText* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma única cadeia de caracteres grande que representa o fluxo de token formatado resultante.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma listagem de erros e avisos que foram encontrados durante a compilação. Essas são as mesmas mensagens que o depurador exibe ao executar no modo de depuração. Esse valor pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXPreprocessShader**](d3dxpreprocessshader.md)
</dt> <dt>

[**D3DXPreprocessShaderFromResource**](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
