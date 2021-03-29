---
title: 'Função RWTexture2DArray:: Load (int, uint)'
description: 'Lê os dados de textura e retorna o status sobre a operação. | Função RWTexture2DArray:: Load (int, uint)'
ms.assetid: 97D6E36A-1613-43BA-92C1-3034E0F344F0
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
ms.openlocfilehash: 969aa0a4efa62f7072c759a1f2188e4d210d8649
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968423"
---
# <a name="rwtexture2darrayloadintuint-function"></a>Função RWTexture2DArray:: Load (int, uint)

Lê os dados de textura e retorna o status sobre a operação.

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

O local da textura.

</dd> <dt>

*Status* \[ do fora\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features). Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwtexture2darray-load.md)
</dt> </dl>

 

 
