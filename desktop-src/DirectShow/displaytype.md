---
description: A função DisplayType envia informações sobre um tipo de mídia para o local de saída de depuração. Ignorado em builds de varejo.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Função DisplayType (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a48bc5f4afbfabc9bdc37ff2cfe8c5890629f3fcaacf135979b82523981ed66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906496"
---
# <a name="displaytype-function"></a>Função DisplayType

A `DisplayType` função envia informações sobre um tipo de mídia para o local de saída de depuração. Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*label* 
</dt> <dd>

Cadeia de caracteres que contém uma mensagem a ser exibida com as informações de tipo de mídia.

</dd> <dt>

*pmtIn* 
</dt> <dd>

ointer para a estrutura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função gera várias mensagens LOG \_ TRACE. No nível de log 2 ou superior, a função exibe o tipo principal, o subtipo e o tipo de formato e os dados do bloco de formato. No nível de log 5 ou superior, a função exibe informações adicionais, como os retângulos de origem e de destino para tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




