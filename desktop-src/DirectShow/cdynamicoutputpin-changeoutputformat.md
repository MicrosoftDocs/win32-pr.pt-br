---
description: O método ChangeOutputFormat altera dinamicamente o tipo de mídia para a conexão e fornece novas informações de segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Método CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755351"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>Método CDynamicOutputPin. ChangeOutputFormat

O `ChangeOutputFormat` método altera dinamicamente o tipo de mídia para a conexão e fornece novas informações de segmento. A alteração pode ocorrer enquanto o grafo de filtro está em execução. Depois que esse método é chamado, os exemplos com o tipo de mídia antigo não podem ser entregues. O chamador deve garantir que nenhuma amostra antiga esteja pendente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

Hora de início do segmento.

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

Hora de parada do segmento.

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

Taxa de segmento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                                                                                                      |
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha. Possivelmente o filtro proprietário não chamou [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN não está conectado.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentários

Esse método altera o tipo de formato enquanto o filtro está em execução. Se o PIN downstream aceitar o novo formato, nenhuma reconexão será necessária. Caso contrário, o método tentará reconectar o PIN. Se o método alterar o formato com êxito, ele entregará as novas informações de segmento. Esse método chama o método [**CDynamicOutputPin:: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) para executar a alteração de formato.

Você deve chamar o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




