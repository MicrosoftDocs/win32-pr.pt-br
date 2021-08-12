---
description: Retornar informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: Método ID3DX10Font::GetGlyphData (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eaabcd6de2acf5ec86ab8c9a47d4224ed230104fe189816abd9d02fd3ac09596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302886"
---
# <a name="id3dx10fontgetglyphdata-method"></a>Método ID3DX10Font::GetGlyphData

Retornar informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
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

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Endereço de um ponteiro para um objeto ID3D10Texture que contém o glifo.

</dd> <dt>

*pBlackBox* \[ Em\]
</dt> <dd>

Tipo: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Ponteiro para o menor objeto retângulo que inclui completamente o glifo. Consulte [RECT](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pCellInc* \[ Em\]
</dt> <dd>

Tipo: **\* POINT**

Ponteiro para o vetor bidimensional que conecta a origem da célula de caractere atual à origem da próxima célula de caractere. Consulte [POINT](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
