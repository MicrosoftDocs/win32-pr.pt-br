---
description: Crie um efeito a partir de uma descrição de efeito ASCII ou binário. Essa função é uma versão estendida do D3DXCreateEffectFromFile que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Função D3DXCreateEffectFromFileEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5f0b329502e6b5e957e1d8c0761fe19fa6bc1e8420269a6329435ba27a53f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526550"
---
# <a name="d3dxcreateeffectfromfileex-function"></a>Função D3DXCreateEffectFromFileEx

Crie um efeito a partir de uma descrição de efeito ASCII ou binário. Essa função é uma versão estendida do [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
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

Ponteiro para o dispositivo que criará o efeito. Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pSrcFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do arquivo. Esse parâmetro dá suporte a cadeias de caracteres Unicode e ANSI. Consulte Observações.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matriz opcional terminada por nulo de definições de macro de pré-processador. Consulte [**D3DXMACRO**](d3dxmacro.md).

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include. Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.

</dd> <dt>

*pSkipConstants* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de parâmetros de efeito que será ignorada pelo sistema de efeito. A cadeia de caracteres deve ser terminada em **nulo** e precisa conter o nome de cada constante gerenciada por aplicativo, separada por um ponto-e-vírgula.

</dd> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se *pSrcFile* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcFile* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX. O compilador do Direct3D 10 HLSL agora é o padrão. Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.

</dd> <dt>

*pPool* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) a ser usado para parâmetros compartilhados. Se esse valor for **NULL**, nenhum parâmetro será compartilhado.

</dd> <dt>

*ppEffect* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Retorna um ponteiro para um buffer que contém o efeito compilado. Consulte [**ID3DXEffect**](id3dxeffect.md).

</dd> <dt>

*ppCompilationErrors* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um ponteiro para um buffer que contém uma lista de erros de compilação. Consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função é uma versão estendida do [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite que um aplicativo especifique quais constantes de efeito serão gerenciadas pelo aplicativo. Uma constante que é gerenciada pelo aplicativo é ignorada pelo sistema de efeitos. Ou seja, o aplicativo é responsável por inicializar a constante, bem como salvar e restaurar seu estado sempre que apropriado.

Essa função verifica cada constante em pSkipConstants para ver que:

-   Ele está associado a um registro constante.
-   Ele só é usado no código do sombreador HLSL.

Se uma constante for nomeada na cadeia de caracteres que não está presente no efeito, ela será ignorada.

Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromFileW. Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
