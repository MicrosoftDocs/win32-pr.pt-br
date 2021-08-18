---
title: Função ByteAddressBuffer::Load3(uint, uint)
description: Obtém três valores e o status da operação.
ms.assetid: 6AD8E957-F646-4749-A9B4-5C0C936D90E3
keywords:
- Função Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db90d9536c069977f07cdb5ca285083314ff200014cefaec8ab874e123a3f52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725340"
---
# <a name="load3uint-uint-function"></a>Função Load3(uint, uint)

Obtém três valores e o status da operação.

## <a name="syntax"></a>Sintaxe

``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **uint**

O endereço de entrada em bytes, que deve ser um múltiplo de 4.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint3**

Três valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[**ByteAddressBuffer**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 