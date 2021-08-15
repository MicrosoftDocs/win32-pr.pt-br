---
title: 'Função Texture2DMSArray:: Load (int, int, int, uint)'
description: 'Lê os dados de textura e retorna o status da operação. | Função Texture2DMSArray:: Load (int, int, int, uint)'
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: c237de43a52650af1d365a6b95c47f51f525b698152b0be0adf2ffe83f15c1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506872"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a>Função Texture2DMSArray:: Load (int, int, int, uint)

Lê os dados de textura e retorna o status da operação.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
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

*sampleindex* \[ no\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O índice de exemplo.

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

O tipo de retorno corresponde ao tipo na declaração para o objeto [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture2dmsarray-load.md)
</dt> <dt>

[**Texture2DMSArray**](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
