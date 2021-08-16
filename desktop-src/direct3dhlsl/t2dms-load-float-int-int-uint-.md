---
title: Função Texture2DMS::Load(int,int,int,uint)
description: Lê dados de textura e retorna o status da operação. | Função Texture2DMS::Load(int,int,int,uint)
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: cb15f420699a9b581a6ac6f498c5e7ff07437ea4371bf1c59b004af1f5a963cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506873"
---
# <a name="texture2dmsloadintintintuint-function"></a>Função Texture2DMS::Load(int,int,int,uint)

Lê dados de textura e retorna o status da operação.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **int2**

As coordenadas de textura.

</dd> <dt>

*sampleindex* \[ Em\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O índice de exemplo.

</dd> <dt>

*Deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int2**

Um deslocamento aplicado às coordenadas de textura antes de carregar.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o [**objeto Texture2DMS.**](sm5-object-texture2dms.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture2dms-load.md)
</dt> <dt>

[**Texture2DMS**](sm5-object-texture2dms.md)
</dt> </dl>

 

 
