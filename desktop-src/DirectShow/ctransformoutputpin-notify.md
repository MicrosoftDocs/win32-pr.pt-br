---
description: Método CTransformOutputPin.Notify – o método Notify notifica o pino de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl::Notify.
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin.Notify (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69cff051ecab1a93d9fdceac20143bef7d1959ff523aa5893e5ae9c633aa80f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538136"
---
# <a name="ctransformoutputpinnotify-method"></a>Método CTransformOutputPin.Notify

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

Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro que recebeu a mensagem de controle de qualidade.

</dd> <dt>

*Q* 
</dt> <dd>

[**Estrutura**](/windows/win32/api/strmif/ns-strmif-quality) de qualidade que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NÃO \_ ENCONTRADO**</dt> </dl> | Não foi possível encontrar um objeto para aceitar a mensagem.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CTransformFilter::AlterQuality do**](ctransformfilter-alterquality.md) filtro. Se o filtro não tratar a mensagem de qualidade, esse método chamará o [**método CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md) no pino de entrada do filtro. O **método PassNotify** passa a mensagem de qualidade upstream (ou para um gerenciador de qualidade personalizado, se um tiver sido instalado).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




