---
title: Função Texture2D::Gather(S,float,int)
description: Retorna os quatro valores de texel que seriam usados em uma operação de filtragem bi-linear. | Função Texture2D::Gather(S,float,int)
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- Função Gather HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 263c3672f55e2f461d9a6c160a60b8222ddeda32ec239b846680d30af0f7fedc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853276"
---
# <a name="texture2dgathersfloatint-function"></a>Função Texture2D::Gather(S,float,int)

Retorna os quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.

## <a name="syntax"></a>Sintaxe

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **sampler**

O índice de amostra baseado em zero.

</dd> <dt>

*local* \[ Em\]
</dt> <dd>

Tipo: **float2**

As coordenadas de exemplo (u,v).

</dd> <dt>

*deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int2**

O deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **TemplateType**

Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.

## <a name="remarks"></a>Comentários

As amostras de textura podem ser usadas para interpolação bilinear.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Coletar métodos](texture2d-gather.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




