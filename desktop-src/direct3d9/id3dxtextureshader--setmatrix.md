---
description: Método ID3DXTextureShader::SetMatrix – define uma matriz não transposta.
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: Método ID3DXTextureShader::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e0d905a3d73bb357e7988f4cc5a749740b796c1793ca912a2f3af471893d65f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729009"
---
# <a name="id3dxtextureshadersetmatrix-method"></a>Método ID3DXTextureShader::SetMatrix

Define uma matriz não transposta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a matriz de constantes. Consulte [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pMatrix* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma matriz não transposta. Consulte [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Uma matriz não transposta contém dados de linha principal; ou seja, cada vetor está contido em uma linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




