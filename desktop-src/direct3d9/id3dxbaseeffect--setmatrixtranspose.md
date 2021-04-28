---
description: 'Método ID3DXBaseEffect:: SetMatrixTranspose – define uma matriz transposeda.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'Método ID3DXBaseEffect:: SetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 384d4a7ed5e1b769218b9290ed6cc0f7f060bd66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107394"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a>Método ID3DXBaseEffect:: SetMatrixTranspose

Define uma matriz transposeda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma matriz transpoda. Consulte [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Uma matriz transpoda contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.

Se a matriz de destino for menor do que a matriz de origem, os componentes adicionais da matriz de origem serão ignorados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




