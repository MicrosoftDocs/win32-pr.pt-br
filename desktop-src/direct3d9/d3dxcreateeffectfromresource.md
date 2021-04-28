---
description: Função D3DXCreateEffectFromResource – crie um efeito de uma descrição de efeito ASCII ou binário.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Função D3DXCreateEffectFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107684"
---
# <a name="d3dxcreateeffectfromresource-function"></a>Função D3DXCreateEffectFromResource

Crie um efeito a partir de uma descrição de efeito ASCII ou binário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para o dispositivo.

</dd> <dt>

*hSrcModule* \[ no\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador para um módulo que contém a descrição do efeito. Se esse parâmetro for **NULL**, o módulo atual será usado.

</dd> <dt>

*pSrcResource* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para o recurso. Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI. Consulte Observações.

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

Se *hSrcModule* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *hSrcModule* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX. O compilador do Direct3D 10 HLSL agora é o padrão. Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.

</dd> <dt>

*pPool* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados. Se esse valor for **NULL**, nenhum parâmetro será compartilhado.

</dd> <dt>

*ppEffect* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Retorna um buffer que contém o efeito compilado.

</dd> <dt>

*ppCompilationErrors* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma lista de erros de compilação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromResourceW. Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.

D3DXCreateEffectFromResource carrega dados de um recurso do tipo RT \_ RCDATA. Consulte o MSDN para obter mais informações sobre os recursos do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
