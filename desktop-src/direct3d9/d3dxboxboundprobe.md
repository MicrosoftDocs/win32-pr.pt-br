---
description: Determina se um raio intersecção do volume da caixa delimitada de uma caixa.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Função D3DXBoxBoundProbe (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 197582c2f404124edd5a49c9d7780ce35cac61b15438a81d120839f283b82373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676386"
---
# <a name="d3dxboxboundprobe-function"></a>Função D3DXBoxBoundProbe

Determina se um raio intersecção do volume da caixa delimitada de uma caixa.

## <a name="syntax"></a>Sintaxe


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMin* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) descrevendo o canto inferior esquerdo da caixa delimitada. Consulte Observações.

</dd> <dt>

*pMax* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) descrevendo o canto superior direito da caixa delimitada. Consulte Observações.

</dd> <dt>

*pRayPosition* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando a coordenada de origem do raio.

</dd> <dt>

*pRayDirection* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) especificando a direção do raio. Esse vetor não deve ser (0,0,0), mas não precisa ser normalizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Retornará **TRUE** se o raio intersecção do volume da caixa delimitada da caixa. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

**D3DXboxBoundProbe** determina se o raio intersecção do volume da caixa delimitada da caixa, não apenas a superfície da caixa.

Os valores passados **para D3DXboxBoundProbe** são xmin, xmax, ymin, ymax, zmin e zmax. Assim, o seguinte define os cantos da caixa delimitada.


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



A profundidade da caixa delimitada na direção z é zmax - zmin, na direção y é ymax - ymin e na direção x é xmax - xmin. Por exemplo, com os seguintes vetores mínimo e máximo, mínimo (-1, -1, -1) e máximo (1, 1, 1), a caixa delimitadora é definida da seguinte maneira.


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
