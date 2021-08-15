---
title: 'Função Texture2D:: Load (int, int, uint)'
description: 'Lê os dados de textura e retorna o status da operação. | Função Texture2D:: Load (int, int, uint)'
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
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
ms.openlocfilehash: 890f49a0609367dcf91c91146f786568fdd83f0f207f7aa69d8dd7c4019b4d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507379"
---
# <a name="texture2dloadintintuint-function"></a>Função Texture2D:: Load (int, int, uint)

Lê os dados de textura e retorna o status da operação.

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

*Local* \[ do no\]
</dt> <dd>

Tipo: **int**

As coordenadas de textura.

</dd> <dt>

*Deslocamento* \[ no\]
</dt> <dd>

Tipo: **int**

Um deslocamento aplicado às coordenadas de textura antes da amostragem.

</dd> <dt>

*Status* \[ do fora\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features). Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**Texture2D**](sm5-object-texture2d.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture2d-load.md)
</dt> </dl>

 

 
