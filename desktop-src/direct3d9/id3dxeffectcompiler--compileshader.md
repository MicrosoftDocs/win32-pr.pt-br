---
description: Compila um sombreador de um efeito que contém uma ou mais funções.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: Método ID3DXEffectCompiler::CompileShader (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343621"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>Método ID3DXEffectCompiler::CompileShader

Compila um sombreador de um efeito que contém uma ou mais funções.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFunction* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a função a ser compilada. Esse valor não deve ser **NULL.** Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pTarget* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador. Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para ver uma lista dos perfis disponíveis.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Compile opções identificadas por vários sinalizadores. O compilador HLSL do Direct3D 10 agora é o padrão. Consulte [Sinalizadores D3DXSHADER](d3dxshader-flags.md) para obter detalhes.

</dd> <dt>

*ppShader* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém o sombreador compilado. O sombreador do compilador é uma matriz de DWORDs. Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém pelo menos a primeira mensagem de erro de compilação que ocorreu. Isso inclui efeitos de erros de compilador e erros de compilação de linguagem de alto nível. Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppConstantTable* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retorna uma interface [**ID3DXConstantTable**](id3dxconstanttable.md) , que pode ser usada para acessar constantes de sombreador. Esse valor pode ser **nulo**. Se você compilar seu aplicativo como grande reconhecimento de endereço (ou seja, usar a opção de vinculador/LARGEADDRESSAWARE para tratar endereços maiores que 2 GB), não poderá usar esse parâmetro e deve defini-lo como **nulo**. Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador que está inserida dentro do sombreador. Nesta chamada **D3DXGetShaderConstantTableEx** , você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK.

Se os argumentos forem inválidos, o método retornará D3DERR \_ INVALIDCALL.

Se o método falhar, o valor de retorno será E \_ falhará.

## <a name="remarks"></a>Comentários

Os destinos podem ser especificados para sombreadores de vértice, sombreadores de pixel e funções de preenchimento de textura.



| Destinos                      | Funções                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| Destinos do sombreador de vértice | vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ sw, vs \_ 3 \_ 0                               |
| Destinos do sombreador de pixel  | ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ \_ 1 3, ps \_ 1 \_ 4, ps \_ 2 \_ 0, ps \_ 2 \_ sw, ps \_ 3 \_ 0 |
| Destinos de preenchimento de textura  | tx \_ 0, tx \_ 1                                                          |



 

Esse método compila um sombreador de uma função que é escrita em uma linguagem semelhante a C. Para obter mais informações, consulte [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
