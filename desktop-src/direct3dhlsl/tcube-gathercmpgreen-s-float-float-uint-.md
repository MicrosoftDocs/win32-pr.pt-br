---
title: Função TextureCube::GatherCmpGreen(S,float,float,uint)
description: Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente verde em relação a um valor de comparação junto com o status de mapeamento de peça. | Função TextureCube::GatherCmpGreen(S,float,float,uint)
ms.assetid: 3EFCEFE1-BFE2-4448-962E-108C3C0861E5
keywords:
- Função GatherCmpGreen HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23d1ede1bcbdcc330b5385c90f0f753888d7248191efc4108a141ad61fc3125b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284870"
---
# <a name="texturecubegathercmpgreensfloatfloatuint-function"></a>Função TextureCube::GatherCmpGreen(S,float,float,uint)

Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente verde em relação a um valor de comparação junto com o status de mapeamento de peça.

## <a name="syntax"></a>Sintaxe


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

*CompareValue* \[ Em\]
</dt> <dd>

Tipo: **float**

Um valor para comparar cada um com cada valor amostrado.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

[Métodos GatherCmpGreen](texturecube-gathercmpgreen.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
