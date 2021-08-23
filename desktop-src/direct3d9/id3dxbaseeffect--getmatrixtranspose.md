---
description: Obtém uma matriz transposta.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: Método ID3DXBaseEffect::GetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59a23e8cde059446dea33d65f90dca9fb7cb2aaf41ab00949e02e34189420b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987776"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a>Método ID3DXBaseEffect::GetMatrixTranspose

Obtém uma matriz transposta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Retorna uma matriz transposta. Consulte [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Uma matriz transposta contém dados de coluna principal; ou seja, cada vetor está contido em uma coluna.

Se a matriz de destino for maior que a matriz de origem, somente os elementos superior esquerdos da matriz de destino serão preenchidos e os componentes restantes da matriz de destino serão definidos como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




