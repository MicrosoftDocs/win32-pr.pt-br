---
description: Define o tipo de luz.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumeração D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 66aefec5d614e5fc51f82741fbb30ace71222997273b7647c0bf51f2d5038878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804771"
---
# <a name="d3dlighttype-enumeration"></a>Enumeração D3DLIGHTTYPE

Define o tipo de luz.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**Ponto de D3DLIGHT \_**
</dt> <dd>

Light é uma fonte de ponto. A luz tem uma posição em espaço e radia a luz em todas as direções.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**Ponto de D3DLIGHT \_**
</dt> <dd>

Light é uma fonte de destaque. Essa luz é como uma luz pontual, exceto que a iluminação é limitada a um cone. Esse tipo de luz tem uma direção e vários outros parâmetros que determinam a forma do cone que ele produz. Para obter informações sobre esses parâmetros, consulte a estrutura [**D3DLIGHT9**](d3dlight9.md) .

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ direcional**
</dt> <dd>

Light é uma fonte de luz direcional. Isso é equivalente a usar uma fonte de luz pontual em uma distância infinita.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

As luzes direcionais são ligeiramente mais rápidas que as fontes de luz do ponto, mas as luzes do ponto parecem um pouco melhores. Os destaques oferecem efeitos visuais interessantes, mas são demorados computacionalmente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




