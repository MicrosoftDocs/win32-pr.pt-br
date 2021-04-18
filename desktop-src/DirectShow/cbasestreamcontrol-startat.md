---
description: 'O método StartAt informa o PIN quando iniciar a entrega de dados. Esse método implementa o método IAMStreamControl:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Método CBaseStreamControl. StartAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752297"
---
# <a name="cbasestreamcontrolstartat-method"></a>Método CBaseStreamControl. StartAt

O `StartAt` método informa o PIN quando iniciar a entrega de dados. Esse método implementa o método [**IAMStreamControl:: StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ptStart* 
</dt> <dd>

Ponteiro para um valor de [**\_ tempo de referência**](reference-time.md) que especifica quando o PIN deve começar a entregar dados.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Especifica um valor a ser enviado junto com a notificação de início.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




