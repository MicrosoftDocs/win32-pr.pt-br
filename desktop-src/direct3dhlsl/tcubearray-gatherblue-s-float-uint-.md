---
title: Função TextureCubeArray::GatherBlue(S,float,uint)
description: Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, juntamente com o status de mapeamento de peças. | Função TextureCubeArray::GatherBlue(S,float,uint)
ms.assetid: 85606EE7-9B05-439F-B525-A1CD42FE32F6
keywords:
- Função GatherBlue HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e61d28596ec84bab024299824ddd57a0979e075b98ef4136072e21420797910a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043164"
---
# <a name="texturecubearraygatherbluesfloatuint-function"></a>Função TextureCubeArray::GatherBlue(S,float,uint)

Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, juntamente com o status de mapeamento de peças.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Tipo: **SamplerState**

O índice de amostra baseado em zero.

</dd> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **float**

As coordenadas de exemplo (u,v).

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

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

[Métodos GatherBlue](texturecubearray-gatherblue.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
