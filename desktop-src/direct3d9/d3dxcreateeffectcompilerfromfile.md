---
description: Função D3DXCreateEffectCompilerFromFile – cria um compilador de efeito a partir de uma descrição de efeito ASCII.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Função D3DXCreateEffectCompilerFromFile (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087974"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a>Função D3DXCreateEffectCompilerFromFile

Cria um compilador de efeito a partir de uma descrição de efeito ASCII.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do arquivo. Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI. Consulte Observações.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Uma matriz opcional com terminação **nula** de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem as definições de pré-processador. Esse valor pode ser **nulo**.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include. Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de compilação identificadas por vários sinalizadores (consulte [sinalizadores D3DXSHADER](d3dxshader-flags.md)). O compilador do Direct3D 10 HLSL agora é o padrão. Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.

</dd> <dt>

*ppEffectCompiler* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , que contém o compilador de efeito.

</dd> <dt>

*ppParseErrors* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , contendo todas as mensagens de erro ocorridas durante a compilação. Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectCompilerFromFileW. Caso contrário, a chamada de função é resolvida como D3DXCreateEffectCompilerFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
