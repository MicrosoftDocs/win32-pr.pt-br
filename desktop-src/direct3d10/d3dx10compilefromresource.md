---
description: Observação em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API D3DCompile. Compilar um sombreador ou um efeito de um recurso.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: Função D3DX10CompileFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812393"
---
# <a name="d3dx10compilefromresource-function"></a>Função D3DX10CompileFromResource

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

Compilar um sombreador ou um efeito de um recurso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSrcModule* \[ no\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador para o módulo de recurso que contém o sombreador. HMODULE pode ser obtido com a [função GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome do recurso que contém o sombreador. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> <dt>

*pSrcFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Opcional. Nome do arquivo de efeito, que é usado somente para mensagens de erro. Pode ser **NULL**.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**

Opcional. Ponteiro para uma matriz de definições de macro (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0. Se não for usado, defina *pDefines* como **nulo**.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Ponteiro para uma interface de [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para manipulação de arquivos de inclusão. Definir isso como **NULL** causará um erro de compilação se um sombreador contiver um \# include.

</dd> <dt>

*pFunctionName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador. Quando você compila um efeito, o **D3DX10CompileFromResource** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.

</dd> <dt>

*pProfile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no [sombreador modelo 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), no [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou no [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).

</dd> <dt>

*Flags1* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Sinalizadores de compilação de sombreador](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md). Quando você compila um sombreador e não um arquivo de efeito, o **D3DX10CompileFromResource** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro não-de-ponto como zero se a função chamada não for usá-lo.

</dd> <dt>

*pPump* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppShader* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém o sombreador compilado, bem como qualquer informação de depuração e tabela de símbolos inserida.

</dd> <dt>

*ppErrorMsgs* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para uma [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém uma listagem de erros e avisos ocorridos durante a compilação. Esses erros e avisos são idênticos à saída de depuração de um depurador.

</dd> <dt>

*pHResult* \[ fora\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL**. Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
