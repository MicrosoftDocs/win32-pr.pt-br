---
description: Função D3DXCompileShader – compilar um arquivo de sombreador.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Função D3DXCompileShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1f5e5f0f30714ed001438235e124341b8ce4d35
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115854"
---
# <a name="d3dxcompileshader-function"></a>Função D3DXCompileShader

Compilar um arquivo de sombreador.

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que contém o sombreador.

</dd> <dt>

*srcDataLen* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Comprimento dos dados em bytes.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Uma matriz terminada **nula** opcional de estruturas [**D3DXMACRO**](d3dxmacro.md) . Esse valor pode ser **nulo**.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Ponteiro de interface opcional, [**ID3DXInclude**](id3dxinclude.md), a ser usado para manipulação de \# diretivas include. Se esse valor for **NULL**, \# incluirá que será respeitado durante a compilação de um arquivo ou causará um erro quando compilado de um recurso ou memória.

</dd> <dt>

*pFunctionName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que contém o nome da função de ponto de entrada do sombreador onde a execução começa.

</dd> <dt>

*pProfile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador. Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obter uma lista dos perfis disponíveis.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de compilação identificadas por vários sinalizadores. O compilador do Direct3D 10 HLSL agora é o padrão. Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.

</dd> <dt>

*ppShader* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém o sombreador criado. Esse buffer contém o código de sombreador compilado, bem como qualquer informação de tabela de depuração e símbolo inserida.

</dd> <dt>

*ppErrorMsgs* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação. Essas são as mesmas mensagens que o depurador exibe ao serem executados no modo de depuração. Esse valor pode ser **nulo**.

</dd> <dt>

*ppConstantTable* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retorna uma interface [**ID3DXConstantTable**](id3dxconstanttable.md) , que pode ser usada para acessar constantes de sombreador. Esse valor pode ser **nulo**. Se você compilar seu aplicativo como grande reconhecimento de endereço (ou seja, usar a opção de vinculador/LARGEADDRESSAWARE para tratar endereços maiores que 2 GB), não poderá usar esse parâmetro e deve defini-lo como **nulo**. Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador que está inserida dentro do sombreador. Nesta chamada **D3DXGetShaderConstantTableEx** , você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
