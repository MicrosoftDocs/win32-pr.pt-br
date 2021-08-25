---
description: Método CBasePin.Notify – o método Notify notifica o pino de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl::Notify.
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Método CBasePin.Notify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910436"
---
# <a name="cbasepinnotify-method"></a>Método CBasePin.Notify

O `Notify` método notifica o pino de que uma alteração de qualidade é solicitada. Esse método implementa o [**método IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSelf* 
</dt> <dd>

Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro que entregue a mensagem de controle de qualidade.

</dd> <dt>

*Q* 
</dt> <dd>

Especifica uma estrutura [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A classe base retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Os pinos de saída devem substituir esse método para aceitar mensagens de controle de qualidade.

Se um gerenciador de qualidade externo tiver sido instalado (consulte [**CBasePin::SetSink),**](cbasepin-setsink.md)passe a mensagem para esse gerenciador de qualidade. Caso contrário, o filtro deve manipular a mensagem em si ou passar a mensagem upstream. Para obter mais informações, consulte [Gerenciamento de controle de qualidade.](quality-control-management.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




