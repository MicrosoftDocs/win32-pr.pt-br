---
description: 'Método CBasePin. Notify – o método Notify notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl:: Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Método CBasePin. Notify (Amfilter. h)
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
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096014"
---
# <a name="cbasepinnotify-method"></a>Método CBasePin. Notify

O `Notify` método notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

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

Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro que forneceu a mensagem de controle de qualidade.

</dd> <dt>

*perguntas* 
</dt> <dd>

Especifica uma estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A classe base retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Os Pins de saída devem substituir esse método para aceitar mensagens de controle de qualidade.

Se um Gerenciador de qualidade externo foi instalado (consulte [**CBasePin:: SetSink**](cbasepin-setsink.md)), passe a mensagem para esse Gerenciador de qualidade. Caso contrário, o filtro deve tratar a própria mensagem ou passar a mensagem upstream. Para obter mais informações, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




