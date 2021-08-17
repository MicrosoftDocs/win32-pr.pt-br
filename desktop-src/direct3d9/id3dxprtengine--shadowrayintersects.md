---
description: Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha. Normalmente usado para determinar se um determinado ponto está em sombra.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'Método ID3DXPRTEngine:: ShadowRayIntersects (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5064e788d89de6e5143ad826a4f61a4afd802931c6964193c8fa46626edf955d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729590"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>Método ID3DXPRTEngine:: ShadowRayIntersects

Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha. Normalmente usado para determinar se um determinado ponto está em sombra.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRayPos* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.

</dd> <dt>

*pRayDir* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção normalizada do raio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retornará **true** se Ray Interseccionar a malha atual; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para definir distâncias mínimas e máximas de interseção com Ray.

Esse método é executado mais rápido que [**ID3DXPRTEngine:: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
