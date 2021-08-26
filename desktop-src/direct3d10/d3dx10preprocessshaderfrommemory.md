---
description: Observação Em vez de usar essa função herdada, recomendamos que você use a API D3DPreprocess. Crie um sombreador de memória sem compilá-lo.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: Função D3DX10PreprocessShaderFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a15bc79c593cbb527d440636d41c88d6d03ce5708e19a6bc961b491853d99116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989126"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a>Função D3DX10PreprocessShaderFromMemory

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess)

 

Crie um sombreador de memória sem compilá-lo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para a memória que contém o sombreador.

</dd> <dt>

*SrcDataSize* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamanho do sombreador.

</dd> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do sombreador.

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

*pPump* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Um ponteiro para uma interface de bomba de thread (consulte Interface [**ID3DX10ThreadPump**](id3dx10threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppShaderText* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para a memória (consulte [**Interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém o sombreador descompilado.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

O endereço de um ponteiro para a memória (consulte [**Interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de criação de efeito, se ocorreu algum.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
