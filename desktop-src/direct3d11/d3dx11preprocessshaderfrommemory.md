---
title: Função D3DX11PreprocessShaderFromMemory (D3DX11async. h)
description: observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Observação em vez de usar essa função, recomendamos que você use a API D3DPreprocess. Crie um sombreador da memória sem compilá-lo.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- Função D3DX11PreprocessShaderFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb626bb01f36ebc93a69c551f038ba82f07a0bd0c07f71093588f6de3cf31f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535981"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a>Função D3DX11PreprocessShaderFromMemory

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .

 

Crie um sombreador da memória sem compilá-lo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Ponteiro para a memória que contém o sombreador.

</dd> <dt>

*SrcDataSize* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

Tamanho do sombreador.

</dd> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome do sombreador.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **\_ \_ macro \* do sombreador D3D11 const**

Uma matriz com terminação nula de macros de sombreador; Defina como **NULL** para não especificar nenhuma macro.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Um ponteiro para uma interface de inclusão; Defina como **NULL** para especificar que não há nenhum arquivo de inclusão.

</dd> <dt>

*pPump* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppShaderText* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Um ponteiro para a memória que contém o sombreador não compilado.

</dd> <dt>

*ppErrorMsgs* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

O endereço de um ponteiro para memória que contém erros de criação de efeito, se houver.

</dd> <dt>

*pHResult* \[ fora\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL**. Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

