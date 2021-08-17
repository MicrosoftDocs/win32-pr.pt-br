---
description: Recupera coordenadas barycentric de texel.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: Método ID3DXTextureGutterHelper::GetBaryMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4183bf9bfa5065595073b8534e978367c3ec16bf76245d639da81292641afa81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729194"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>Método ID3DXTextureGutterHelper::GetBaryMap

Recupera coordenadas barycentric de texel.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBaryData* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que contém as duas primeiras coordenadas barycentric de cada texel.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A terceira coordenada barycentric é dada por:


```
    1 - ( pBaryData.x + pBaryData.y )
```



As coordenadas barycentric são sempre especificadas em relação ao triângulo retornado por [**ID3DXTextureGutterHelper::GetFaceMap.**](id3dxtexturegutterhelper--getfacemap.md)

As coordenadas barycentric retornadas por esse método são válidas somente para os texels válidos (não classe 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para os texels válidos.

[**Os texels de classe 2**](id3dxtexturegutterhelper.md) são mapeados para o ponto mais próximo no triângulo no espaço de texel.

O aplicativo deve alocar e gerenciar pBaryData.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas centradas em barras, consulte Descrição de [coordenadas barycentric da Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




