---
description: Função D3DXCompileShaderFromFile – Compilar um arquivo de sombreador.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: Função D3DXCompileShaderFromFile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65c9ac4d958f68aee8a958828c7cb54b5bec408afac1dfed8206ce6aa05dc4ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750446"
---
# <a name="d3dxcompileshaderfromfile-function"></a>Função D3DXCompileShaderFromFile

Compile um arquivo de sombreador.

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
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

*pSrcFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.

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

*pFunctionName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para a função de ponto de entrada do sombreador em que a execução começa.

</dd> <dt>

*pProfile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador. Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para ver uma lista dos perfis disponíveis.

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

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retorna uma [**interface ID3DXConstantTable,**](id3dxconstanttable.md) que pode ser usada para acessar constantes de sombreador. Esse valor pode ser **NULL.** Se você compilar seu aplicativo como um grande reconhecedor de endereço (ou seja, usar a opção de vinculador /LARGEADDRESSAWARE para lidar com endereços maiores que 2 GB), você não poderá usar esse parâmetro e deverá defini-lo como **NULL.** Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador inserida dentro do sombreador. Nesta chamada **D3DXGetShaderConstantTableEx,** você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *Flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ NOTIMPL, E \_ OUTOFMEMORY.

E NOTIMPL será retornado se você estiver usando sombreadores \_ 1.1 \_ (versus 1 \_ 1 e ps \_ 1 \_ 1).

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

 

 
