---
description: 'O método Unadvise remove uma solicitação de aviso pendente. Esse método implementa o método IReferenceClock:: Unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Método CBaseReferenceClock. Unadvise (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751906"
---
# <a name="cbasereferenceclockunadvise-method"></a>Método CBaseReferenceClock. Unadvise

O `Unadvise` método remove uma solicitação de aviso pendente. Esse método implementa o método [**IReferenceClock:: Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwAdviseToken* 
</dt> <dd>

Identificador da solicitação a ser removida. Use o valor retornado pelos métodos [**CBaseReferenceClock:: aconselhetime**](cbasereferenceclock-advisetime.md) ou [**CBaseReferenceClock:: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) no parâmetro *pdwAdviseToken* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Não encontrado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




