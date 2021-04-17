---
description: Recupera as coordenadas Texel barycentric.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'Método ID3DXTextureGutterHelper:: GetBaryMap (D3DX9Mesh. h)'
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
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811713"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>Método ID3DXTextureGutterHelper:: GetBaryMap

Recupera as coordenadas Texel barycentric.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBaryData* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que contém as duas primeiras coordenadas barycentric de cada Texel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A terceira coordenada barycentric é fornecida por:


```
    1 - ( pBaryData.x + pBaryData.y )
```



As coordenadas barycentric são sempre especificadas em relação ao triângulo retornado por [**ID3DXTextureGutterHelper:: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).

As coordenadas de Barycentric retornadas por esse método são válidas somente para texels válidas (não classe 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para texels válidas.

A [**classe 2 texels**](id3dxtexturegutterhelper.md) são mapeadas para o ponto mais próximo no triângulo no espaço Texel.

O aplicativo deve alocar e gerenciar pBaryData.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




