---
description: Aplica medianizes a um buffer de textura flutuante.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'Método ID3DXTextureGutterHelper:: ApplyGuttersFloat (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c0401a6d0692331adf9e80c800530690e59eeec5e6a9463b57425af1a3f9330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800359"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>Método ID3DXTextureGutterHelper:: ApplyGuttersFloat

Aplica medianizes a um buffer de textura flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDataIn* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para um buffer de dados de textura FLOAT.

</dd> <dt>

*NumCoeffs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de escalares por canal de cor usado na memória para armazenar amostras. Cada Texel contém valores FLOAT NumCoeffs.

</dd> <dt>

*Largura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Largura da textura, em pixels, Obtida de [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md).

</dd> <dt>

*Altura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Altura da textura, em pixels, Obtida de [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A [**classe 2 texels**](id3dxtexturegutterhelper.md) são geradas pela reamostração da classe 1 e 4 texels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
