---
title: 'Função RWBuffer:: Load (int, uint)'
description: 'Lê os dados de buffer e retorna o status da operação. | Função RWBuffer:: Load (int, uint)'
ms.assetid: 90C9ECE8-2068-47C7-B87A-941B2D4F221D
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
ms.openlocfilehash: 81d23d67b0d02ed375e07f310089067d6a7bbd67
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091905"
---
# <a name="rwbufferloadintuint-function"></a>Função RWBuffer:: Load (int, uint)

Lê os dados de buffer e retorna o status da operação.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Local* \[ do no\]
</dt> <dd>

Tipo: **int**

O local do buffer.

</dd> <dt>

*Status* \[ do fora\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features). Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWBuffer**](sm5-object-rwbuffer.md) .

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwbuffer-load.md)
</dt> </dl>

 

 
