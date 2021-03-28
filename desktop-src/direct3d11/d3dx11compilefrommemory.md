---
title: Função D3DX11CompileFromMemory (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API D3DCompile. Compile um sombreador ou um efeito que é carregado na memória.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- Função D3DX11CompileFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968634"
---
# <a name="d3dx11compilefrommemory-function"></a>Função D3DX11CompileFromMemory

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .

 

Compile um sombreador ou um efeito que é carregado na memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Ponteiro para o sombreador na memória.

</dd> <dt>

*SrcDataLen* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

Tamanho do sombreador na memória.

</dd> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome do arquivo que contém o código do sombreador.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **\* [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**

Opcional. Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0. Se não for usado, defina *pDefines* como **nulo**.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Ponteiro para uma interface para manipulação de arquivos de inclusão. Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.

</dd> <dt>

*pFunctionName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador. Quando você compila um efeito, o **D3DX11CompileFromMemory** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.

</dd> <dt>

*pProfile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no sombreador modelo 2, o Shader Model 3, o Shader Model 4 ou o Shader Model 5. O perfil também pode ser para o tipo de efeito (por exemplo, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-constants)de sombreador.

</dd> <dt>

*Flags2* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Sinalizadores de compilação**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efeito. Quando você compila um sombreador e não um arquivo de efeito, o **D3DX11CompileFromMemory** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.

</dd> <dt>

*pPump* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppShader* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para a memória que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.

</dd> <dt>

*ppErrorMsgs* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para memória que contém uma lista de erros e avisos ocorridos durante a compilação. Esses erros e avisos são idênticos à saída de depuração de um depurador.

</dd> <dt>

*pHResult* \[ fora\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL**. Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

**D3DX11CompileFromMemory** retornará E \_ INVALIDARG se você fornecer não **nulo** ao parâmetro *pHResult* quando fornecer **NULL** para o parâmetro *pPump* . Para obter mais informações sobre essa situação, consulte comentários.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre **D3DX11CompileFromMemory**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Você deve fornecer **NULL** para o parâmetro *pHResult* se também fornecer **NULL** para o parâmetro *pPump* . Caso contrário, você não poderá criar um sombreador subsequentemente usando o código do sombreador compilado que o **D3DX11CompileFromMemory** retorna na memória à qual o parâmetro *ppShader* aponta. Para criar um sombreador do código de sombreador compatível, você chama um dos seguintes métodos de interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Além disso, se você fornecer um valor não **nulo** para *pHResult* quando você fornecer **NULL** para *pPump*, **D3DX11CompileFromMemory** retornará o código de \_ erro E INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

