---
description: 'Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h) – carrega a identidade na matriz atual.'
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 046267b11f1a2aa977eda7f5fe461e5c44a2cf59e1f50ae291cf714f063088c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847736"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: loadidentity (D3dx9math. h)

Carrega a identidade na matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A matriz de identidade é uma matriz na qual todos os coeficientes são 0,0, exceto os \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, os \] coeficientes, que são definidos como 1,0. A matriz de identidade é especial quando ela é aplicada a vértices, elas não são alteradas. A matriz de identidade é usada como ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: loadmatrix**](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




