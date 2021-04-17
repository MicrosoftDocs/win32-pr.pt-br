---
description: Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'Método ID3DXFont:: GetGlyphData (D3dx9core. h)'
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
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762063"
---
# <a name="id3dxfontgetglyphdata-method"></a>Método ID3DXFont:: GetGlyphData

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

*Glifo* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de glifo.

</dd> <dt>

*ppTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Endereço de um ponteiro para um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que contém o glifo.

</dd> <dt>

*pBlackBox* \[ fora\]
</dt> <dd>

Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Ponteiro para o menor objeto Rectangle que inclui completamente o glifo.

</dd> <dt>

*pCellInc* \[ fora\]
</dt> <dd>

Tipo: **[ **ponto**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor bidimensional que conecta a origem da célula de caractere atual à origem da próxima célula de caractere. Consulte o [**ponto**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
