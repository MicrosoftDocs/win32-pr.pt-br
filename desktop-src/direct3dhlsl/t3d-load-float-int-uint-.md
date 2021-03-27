---
title: 'Função Texture3D:: Load (int, int, uint)'
description: 'Lê os dados de textura e retorna o status da operação. | Função Texture3D:: Load (int, int, uint)'
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
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
ms.openlocfilehash: 19522fe60567e55565265ce0c8b5051c7bf7ccdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989144"
---
# <a name="texture3dloadintintuint-function"></a>Função Texture3D:: Load (int, int, uint)

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

## <a name="return-value"></a>Retornar valor

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**Texture3D**](sm5-object-texture3d.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture3d-load.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
