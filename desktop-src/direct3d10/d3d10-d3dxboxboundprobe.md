---
description: A função D3DXBoxBoundProbe (D3DX10math. h) determina se um raio intersecciona o volume da caixa delimitadora de uma caixa.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Função D3DXBoxBoundProbe (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187815"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>Função D3DXBoxBoundProbe (D3DX10math. h)

Determina se um raio intersecciona o volume da caixa delimitadora de uma caixa.

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

*pMin* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que descreve o canto inferior esquerdo da caixa delimitadora. Consulte Observações.

</dd> <dt>

*pMax* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , descrevendo o canto superior direito da caixa delimitadora. Consulte Observações.

</dd> <dt>

*pRayPosition* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3, especificando a coordenada de origem do raio.

</dd> <dt>

*pRayDirection* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3, especificando a direção do raio. Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da caixa. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

**D3DXBoxBoundProbe** determina se o raio intersecciona o volume da caixa delimitadora da caixa, não apenas a superfície da caixa.

Os valores passados para **D3DXBoxBoundProbe** são xmin, xMax, ymin, ymax, zmin e Zmax. Portanto, o seguinte define os cantos da caixa delimitadora.


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



A profundidade da caixa delimitadora na direção z é Zmax-zmin, na direção y, ymax-ymin e, na direção x, é xmax-xmin. Por exemplo, com os seguintes vetores mínimo e máximo, min (-1,-1,-1) e Max (1, 1, 1), a caixa delimitadora é definida da maneira a seguir.


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
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro  | D3DX10math. h |
| Biblioteca | D3DX10. lib  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
