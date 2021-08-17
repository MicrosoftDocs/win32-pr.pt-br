---
title: Função RWByteAddressBuffer::Load3(uint,uint)
description: Obtém três valores e retorna o status da operação.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
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
ms.openlocfilehash: 91d4a90094d93705e17c9087583974ef8f9d76e1878cb0c5aa8dab21dc82e073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791218"
---
# <a name="load3uintuint-function"></a>Função Load3(uint,uint)

Obtém três valores e retorna o status da operação.

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

O local do buffer.

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
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load3](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 