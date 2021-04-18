---
description: 'O método getTime recupera os tempos de transmissão em que este exemplo deve começar e terminar. Esse método implementa o método IMediaSample:: getTime.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Método CMediaSample. getTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756628"
---
# <a name="cmediasamplegettime-method"></a>Método CMediaSample. getTime

O `GetTime` método recupera os tempos de transmissão em que este exemplo deve começar e terminar. Esse método implementa o método [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início do fluxo, em unidades de 100 nanossegundos.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora final do fluxo, em unidades de 100 nanossegundos. Se o exemplo não tiver hora de parada, o valor será definido como a hora de início mais um.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                   | Descrição                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Êxito.<br/>                                         |
| <dl> <dt>**VFW \_ S \_ sem \_ hora de parada \_**</dt> </dl>         | O exemplo tem uma hora de início válida, mas nenhuma hora de parada.<br/> |
| <dl> <dt>**VFW \_ E \_ tempo de amostra \_ \_ não \_ definido**</dt> </dl> | O exemplo não tem carimbos de data/hora válidos.<br/>          |



 

## <a name="remarks"></a>Comentários

As variáveis de membro end [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample:: m \_**](cmediasample-m-end.md) especificam os carimbos de data/hora. A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica se os carimbos de data/hora são válidos.

Para obter informações sobre carimbos de data/hora, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




