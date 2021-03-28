---
title: 'Função RWTexture2D:: Load (int)'
description: 'Lê dados de textura. | Função RWTexture2D:: Load (int)'
ms.assetid: AEBB9C78-BE4B-4121-93CC-EE03B9925CF0
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab5f8d755ad4af3127a0c238defc9f1c422061bc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989204"
---
# <a name="rwtexture2dloadint-function"></a>Função RWTexture2D:: Load (int)

Lê dados de textura.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Local* \[ do no\]
</dt> <dd>

Tipo: **int**

O local da textura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture2D**](sm5-object-rwtexture2d.md) .

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwtexture2d-load.md)
</dt> </dl>

 

 




