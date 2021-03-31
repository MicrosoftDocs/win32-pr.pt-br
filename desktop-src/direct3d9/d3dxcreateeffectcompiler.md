---
description: Cria um compilador de efeito a partir de uma descrição de efeito ASCII.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Função D3DXCreateEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664083"
---
# <a name="d3dxcreateeffectcompiler-function"></a>Função D3DXCreateEffectCompiler

Cria um compilador de efeito a partir de uma descrição de efeito ASCII.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que contém uma descrição de efeito.

</dd> <dt>

*SrcDataLen* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Comprimento, em bytes, dos dados de efeito.

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

Endereço de um ponteiro para uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contém o compilador de efeito.

</dd> <dt>

*ppParseErrors* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) que contém as mensagens de erro ocorridas durante a compilação. Esse parâmetro pode ser definido como **nulo** para ignorar mensagens de erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
