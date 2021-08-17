---
title: Função Texture1D::Load(int,int,uint)
description: Lê dados de textura e retorna o status da operação. | Função Texture1D::Load(int,int,uint)
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
keywords:
- Função de carregamento HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b266ad13c050073aeb62497d9833b1f2666e70f2f32f2f9de5099cf4bee29517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722987"
---
# <a name="texture1dloadintintuint-function"></a>Função Texture1D::Load(int,int,uint)

Lê dados de textura e retorna o status da operação.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **int**

As coordenadas de textura.

</dd> <dt>

*Deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int**

Um deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o [**objeto Texture1D.**](sm5-object-texture1d.md)

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture1d-load.md)
</dt> <dt>

[**Texture1D**](sm5-object-texture1d.md)
</dt> </dl>

 

 
