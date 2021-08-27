---
title: Função StructuredBuffer::Load(int,uint)
description: Lê dados de buffer e retorna o status sobre a operação. | Função StructuredBuffer::Load(int,uint)
ms.assetid: d71c6057-6651-4b70-91cf-892fde6d0188
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
ms.openlocfilehash: 76e710a4d43c04f8b00b19522d274c66c7acade03387026388dc1a9c6f37ac67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094956"
---
# <a name="structuredbufferloadintuint-function"></a>Função StructuredBuffer::Load(int,uint)

Lê dados de buffer e retorna o status sobre a operação.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **int**

O local do buffer.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para [**o objeto StructuredBuffer.**](sm5-object-structuredbuffer.md)

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](structuredbuffer-load.md)
</dt> </dl>

 

 
