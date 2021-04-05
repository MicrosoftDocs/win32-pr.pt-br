---
description: Cria um objeto de fonte para um dispositivo e uma fonte.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Função D3DXCreateFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664053"
---
# <a name="d3dxcreatefont-function"></a>Função D3DXCreateFont

Cria um objeto de fonte para um dispositivo e uma fonte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado ao objeto Font.

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

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O conjunto de caracteres da fonte.

</dd> <dt>

*OutputPrecision* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica como o Windows deve tentar corresponder os tamanhos de fonte e as características desejadas com as fontes reais. Use \_ apenas TT \_ \_ precis por exemplo, para garantir que sempre obtenha uma fonte TrueType.

</dd> <dt>

*Qualidade* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica como o Windows deve corresponder à fonte desejada com uma fonte real. Ele se aplica somente a fontes rasterizadas e não deve afetar as fontes TrueType.

</dd> <dt>

*PitchAndFamily* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de densidade e família.

</dd> <dt>

*pFacename* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome da face de tipos. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados String será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*ppFont* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Retorna um ponteiro para uma interface [**ID3DXFont**](id3dxfont.md) , representando o objeto Font criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A criação de um objeto ID3DXFont requer que o dispositivo dê suporte à cor de 32 bits.

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontW. Caso contrário, a chamada de função é resolvida como D3DXCreateFontA porque as cadeias de caracteres ANSI estão sendo usadas.

Se você quiser obter mais informações sobre parâmetros de fonte, consulte [a fonte lógica](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
