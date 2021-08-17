---
description: Observação Em vez de usar essa função herdada, recomendamos que você use a API D3DPreprocess. Crie um sombreador de um arquivo sem compilá-lo.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: Função D3DX10PreprocessShaderFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e227ebf001e1af6beac21403d93201c758a63acf96aa5e1daa78b1c8fa506654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128348"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a>Função D3DX10PreprocessShaderFromFile

> [!Note]  
> Em vez de usar essa função herdada, recomendamos que você use a API [**D3DPreprocess.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess)

 

Crie um sombreador de um arquivo sem compilá-lo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome do arquivo de sombreador.

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
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
