---
description: Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h) – carrega a identidade na matriz atual.
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 26d52ca8bd8ebccf04a3f2e4f36e35a1ac4e5b2b74d8c0e0a79bd9b85568cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736055"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h)

Carrega a identidade na matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A matriz de identidade é uma matriz na qual todos os coeficientes são 0,0, exceto os \[ coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, que são \] definidos como 1,0. A matriz de identidade é especial porque, quando ela é aplicada aos vértices, elas ficam inalteradas. A matriz de identidade é usada como o ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




