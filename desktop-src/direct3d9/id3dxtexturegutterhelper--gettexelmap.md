---
description: Recupera as coordenadas de textura (u, v) de cada Texel.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'Método ID3DXTextureGutterHelper:: GetTexelMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298649"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a>Método ID3DXTextureGutterHelper:: GetTexelMap

Recupera as coordenadas de textura (u, v) de cada Texel.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexelData* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para o local em coordenadas de textura de pixel (u, v) onde cada Texel está localizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

Para a [**classe 2 e 4 texels**](id3dxtexturegutterhelper.md), as coordenadas de textura retornadas (u, v) correspondem ao ponto mais próximo no triângulo mais próximo.

O aplicativo deve alocar e gerenciar pTexelData.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




