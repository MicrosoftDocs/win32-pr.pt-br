---
description: Cria um objeto de fonte para um dispositivo e uma fonte. Observação em vez de usar essa função, recomendamos que você use DirectWrite e a biblioteca DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Função D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807875"
---
# <a name="d3dx10createfont-function"></a>Função D3DX10CreateFont

Cria um objeto de fonte para um dispositivo e uma fonte.

> [!Note]  
> Em vez de usar essa função, recomendamos que você use [DirectWrite](../directwrite/direct-write-portal.md) e a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ponteiro para uma interface ID3D10Device, o dispositivo a ser associado ao objeto Font.

</dd> <dt>

*Altura* \[ no\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

A altura dos caracteres em unidades lógicas.

</dd> <dt>

*Largura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

A largura dos caracteres em unidades lógicas.

</dd> <dt>

*Peso* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Espessura da face de tipos. Um exemplo é negrito.

</dd> <dt>

*MipLevels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de níveis de mipmap.

</dd> <dt>

*Itálico* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

True para a fonte em itálico; caso contrário, false.

</dd> <dt>

Conjunto de *caracteres* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O conjunto de caracteres da fonte.

</dd> <dt>

*OutputPrecision* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica como o Windows deve tentar corresponder os tamanhos de fonte e as características desejadas com as fontes reais. Use \_ apenas TT \_ \_ precis por exemplo, para garantir que sempre obtenha uma fonte TrueType.

</dd> <dt>

*Qualidade* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica como o Windows deve corresponder à fonte desejada com uma fonte real. Ele se aplica somente a fontes rasterizadas e não deve afetar as fontes TrueType.

</dd> <dt>

*PitchAndFamily* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de densidade e família.

</dd> <dt>

*pFaceName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome da face de tipos. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*ppFont* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Retorna um ponteiro para uma interface ID3DX10Font, representando o objeto Font criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontW. Caso contrário, a chamada de função é resolvida como D3DXCreateFontA porque as cadeias de caracteres ANSI estão sendo usadas.

Se você quiser obter mais informações sobre parâmetros de fonte, consulte [a fonte lógica](/previous-versions//ms533985(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
