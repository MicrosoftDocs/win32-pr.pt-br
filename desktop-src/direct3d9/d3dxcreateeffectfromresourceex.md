---
description: Crie um efeito a partir de uma descrição de efeito ASCII ou binário. Esta é uma versão estendida do D3DXCreateEffectFromResource que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Função D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788623"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a>Função D3DXCreateEffectFromResourceEx

Crie um efeito a partir de uma descrição de efeito ASCII ou binário. Esta é uma versão estendida do [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite que um aplicativo controle quais parâmetros são ignorados pelo sistema de efeitos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
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

*pSkipConstants* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de parâmetros de efeito que será ignorada pelo sistema de efeito. A cadeia de caracteres deve ser terminada em **nulo** e precisa conter o nome de cada constante gerenciada por aplicativo, separada por um ponto-e-vírgula.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se *pSrcResource* contiver um efeito de texto, os sinalizadores poderão ser uma combinação de sinalizadores [D3DXSHADER](d3dxshader-flags.md) e sinalizadores [D3DXFX](d3dxfx.md) ; caso contrário, *pSrcResource* conterá um efeito binário e os únicos sinalizadores honrados serão sinalizadores D3DXFX. O compilador do Direct3D 10 HLSL agora é o padrão. Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.

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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função é uma versão estendida do [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite que um aplicativo especifique quais constantes de efeito serão gerenciadas pelo aplicativo. Uma constante que é gerenciada pelo aplicativo é ignorada pelo sistema de efeitos. Ou seja, o aplicativo é responsável por inicializar a constante, bem como salvar e restaurar seu estado sempre que apropriado.

Essa função verifica cada constante em pSkipConstants para ver que:

-   Ele está associado a um registro constante.
-   Ele só é usado no código do sombreador HLSL.

Se uma constante for nomeada na cadeia de caracteres que não está presente no efeito, ela será ignorada.

Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados LPCTSTR será resolvido para LPCSTR.

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateEffectFromResourceW. Caso contrário, a chamada de função é resolvida como D3DXCreateEffectFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.

D3DXCreateEffectFromResource carrega dados de um recurso do tipo RT \_ RCDATA. Consulte o MSDN para obter mais informações sobre os recursos do Windows.

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

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
