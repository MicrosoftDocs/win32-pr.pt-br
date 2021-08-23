---
description: Cria um ID3DXEffectCompiler de uma descrição de efeito ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Função D3DXCreateEffectCompilerFromResource (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8f781137e6da118392f8b4e17addd92123b75ecd994191a86ab74d46f3dde6f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045164"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a>Função D3DXCreateEffectCompilerFromResource

Cria um [**ID3DXEffectCompiler de**](id3dxeffectcompiler.md) uma descrição de efeito ASCII.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
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

Ponteiro para o recurso. Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI. Consulte Observações.

</dd> <dt>

*pDefines* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Uma matriz **opcional terminada** em NULL de estruturas [**D3DXMACRO**](d3dxmacro.md) que descrevem definições de pré-processador. Esse valor pode ser **NULL.**

</dd> <dt>

*pInclude* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para lidar com \# diretivas de inclusão. Se esse valor for **NULL,** includes serão honorados ao compilar de um arquivo ou causarão um erro quando compilados de um recurso \# ou memória.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Compilar opções identificadas por vários sinalizadores (consulte [Sinalizadores D3DXSHADER](d3dxshader-flags.md)). O compilador HLSL do Direct3D 10 agora é o padrão. Consulte [Effect-Compiler Tool para](../direct3dtools/fxc.md) obter detalhes.

</dd> <dt>

*ppEffectCompiler* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler,**](id3dxeffectcompiler.md) que contém o compilador de efeito.

</dd> <dt>

*ppParseErrors* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer,**](id3dxbuffer.md) contendo todas as mensagens de erro ocorridas durante a compilação. Esse parâmetro pode ser definido como **NULL para** ignorar mensagens de erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXCreateEffectCompilerFromResourceW. Caso contrário, a chamada de função será resolvida para D3DXCreateEffectCompilerFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
