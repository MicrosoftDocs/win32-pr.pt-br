---
title: Função RWTexture3D::Operator
description: Retorna uma variável de recurso de um RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
keywords:
- Função de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8db7073ef20976ecb6c39839d5639a1f0fcfe1fad765c2cf9b0ecdf086622b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509132"
---
# <a name="rwtexture3doperator--function"></a>Função RWTexture3D::Operator

Retorna uma variável de recurso [**de um RWTexture3D.**](sm5-object-rwtexture3d.md)

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ Em\]
</dt> <dd>

Tipo: **uint3**

A posição do índice. Contém as coordenadas (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




