---
description: Crie um processador de dados assíncronos para um sombreador.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Função D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: f5e7011d868b46196293f441d76d182156fb0ba1431227d6bf01212f8c809249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303461"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a>Função D3DX10CreateAsyncCompilerProcessor

Crie um processador de dados assíncronos para um sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que contém o nome de arquivo do sombreador.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**

Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Este parâmetro pode ser **NULL**.

</dd> <dt>

*pFunctionName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da função de ponto de entrada do sombreador em que começa a execução do sombreador. Quando você compila um efeito, o **D3DX10CreateAsyncCompilerProcessor** ignora *pFunctionName*; Recomendamos que você defina *pFunctionName* como **NULL** porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.

</dd> <dt>

*pProfile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) ou o modelo de sombreador.

</dd> <dt>

*Flags1* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Sinalizadores de compilação de sombreador](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Sinalizadores de compilação de efeito](d3d10-graphics-reference-effect-constants.md). Quando você compila um sombreador e não um arquivo de efeito, o **D3DX10CreateAsyncCompilerProcessor** ignora *Flags2*; é recomendável que você defina *Flags2* como zero porque é uma boa prática de programação definir um parâmetro de ponteiro como **nulo** se a função chamada não o usar.

</dd> <dt>

*ppCompiledShader* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um ponteiro para o efeito compilado (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppErrorBuffer* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um ponteiro para erros de compilação (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppDataProcessor* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

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

 

 
