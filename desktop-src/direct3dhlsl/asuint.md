---
title: função asuint
description: Reinterpreta o padrão de bit de um valor de 64 bits como dois inteiros de 32 bits não assinados.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- função asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006696"
---
# <a name="asuint-function"></a>função asuint

Reinterpreta o padrão de bit de um valor de 64 bits como dois inteiros de 32 bits não assinados.

## <a name="syntax"></a>Sintaxe

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **duplo**

O valor de entrada.

</dd> <dt>

*lowbits* \[ fora\]
</dt> <dd>

Tipo: **uint**

O padrão de *valor* baixo de 32 bits.

</dd> <dt>

*highbits* \[ fora\]
</dt> <dd>

Tipo: **uint**

O padrão de *valor* alto de 32 bits.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função é uma versão alternativa do [**asuint**](dx-graphics-hlsl-asuint.md) intrínseco que está disponível em modelos de sombreador anteriores e foi introduzida para o modelo de sombreador 5. A função original (reconhecida no compilador HLSL por sua assinatura diferente) permanece disponível para o modelo de sombreador 5.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




