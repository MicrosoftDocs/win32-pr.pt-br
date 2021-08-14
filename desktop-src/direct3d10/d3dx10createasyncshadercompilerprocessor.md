---
description: Compile um sombreador e crie um processador de dados de forma assíncrona.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: Função D3DX10CreateAsyncShaderCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: d11142b1e180f7194c569fc55d11fba023e53c2a9d9f5ae5db2a39e809cbc13c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281566"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a>Função D3DX10CreateAsyncShaderCompilerProcessor

Compile um sombreador e crie um processador de dados de forma assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que contém o nome do arquivo do sombreador.

</dd> <dt>

*pDefines* \[ Em\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Uma matriz terminada em NULL de macros de sombreador (consulte  MACRO DO [**\_ SOMBREADOR \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); de definido como NULL para não especificar macros.

</dd> <dt>

*pInclude* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Um ponteiro para uma interface de inclusão (consulte [**Interface ID3D10Incluir**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); de definido como **NULL** para especificar que não há nenhum arquivo de inclusão.

</dd> <dt>

*pFunctionName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da função de ponto de entrada para o sombreador.

</dd> <dt>

*pProfile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que especifica o [perfil do sombreador ou](../direct3dhlsl/dx-graphics-hlsl-models.md) o modelo de sombreador.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opções de compilação HLSL (consulte [Sinalizadores de sombreador](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*ppCompiledShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um ponteiro para o sombreador compilado. Consulte [**Interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um ponteiro para um buffer que contém erros de compilação (consulte Interface [**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte Interface [**ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

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

 

 
