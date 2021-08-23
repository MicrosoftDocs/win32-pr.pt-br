---
description: Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: Método ID3DXFont::GetGlyphData (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7981e10497dc263a60ae2d5e176fd4d95746b3193d7a5b606aea16afa1188ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629885"
---
# <a name="id3dxfontgetglyphdata-method"></a>Método ID3DXFont::GetGlyphData

Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Glifo* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de glifo.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Endereço de um ponteiro para um [**objeto IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que contém o glifo.

</dd> <dt>

*pBlackBox* \[ out\]
</dt> <dd>

Tipo: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Ponteiro para o menor objeto retângulo que inclui completamente o glifo.

</dd> <dt>

*pCellInc* \[ out\]
</dt> <dd>

Tipo: **[ **POINT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor bidimensional que conecta a origem da célula de caractere atual à origem da próxima célula de caractere. Consulte [**POINT**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
