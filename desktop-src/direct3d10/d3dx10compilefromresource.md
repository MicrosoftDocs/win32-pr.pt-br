---
description: Observação Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API D3DCompile. Compile um sombreador ou um efeito de um recurso.
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
ms.openlocfilehash: 2c938ca302e21be16dfd1d2700a80e0ee350d7acb52ce7ab72fe2c52cbae4bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634926"
---
# <a name="d3dx10compilefromresource-function"></a>Função D3DX10CompileFromResource

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use a API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

 

Compile um sombreador ou um efeito de um recurso.

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

*hSrcModule* \[ Em\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Lidar com o módulo de recurso que contém o sombreador. HMODULE pode ser obtido com a [função GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome do recurso que contém o sombreador. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> <dt>

*pSrcFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Opcional. Nome do arquivo de efeito, que é usado apenas para mensagens de erro. Pode ser **NULL.**

</dd> <dt>

*pDefines* \[ Em\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Opcional. Ponteiro para uma matriz de definições de macro (consulte [**MACRO DO SOMBREADOR D3D \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). A última estrutura na matriz serve como um terminador e deve ter todos os membros definidos como 0. Se não for usado, *defina pDefines* como **NULL.**

</dd> <dt>

*pInclude* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Ponteiro para uma [**interface ID3D10Incluir Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para lidar com arquivos de inclusão. Definir isso como **NULL** causará um erro de compilação se um sombreador contiver uma \# inclusão.

</dd> <dt>

*pFunctionName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da função de ponto de entrada do sombreador em que a execução do sombreador começa. Quando você compila um efeito, **D3DX10CompileFromResource** ignora *pFunctionName*; É recomendável definir *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **NULL** se a função chamada não o usar.

</dd> <dt>

*pProfile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que especifica o modelo de sombreador; pode ser qualquer perfil no [modelo de sombreador 2,](../direct3dhlsl/dx-graphics-hlsl-sm2.md)modelo [de sombreador 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou [modelo de sombreador 4.](../direct3dhlsl/dx-graphics-hlsl-sm4.md)

</dd> <dt>

*Sinalizadores1* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Sinalizadores de compilação do sombreador](d3d10-shader.md).

</dd> <dt>

*Sinalizadores2* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md). Quando você compila um sombreador e não um arquivo de efeito, **D3DX10CompileFromResource** ignora *Flags2*; É recomendável definir *Flags2* como zero porque é uma boa prática de programação definir um parâmetro nãopointer como zero se a função chamada não o usar.

</dd> <dt>

*pPump* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Um ponteiro para uma interface de bomba de thread (consulte Interface [**ID3DX10ThreadPump**](id3dx10threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para uma [**Interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém o sombreador compilado, bem como informações de depuração e tabela de símbolos inseridas.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para uma [**Interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contém uma lista de erros e avisos que ocorreram durante a compilação. Esses erros e avisos são idênticos à saída de depuração de um depurador.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL.** Se *pPump* não for **NULL,** *o pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
