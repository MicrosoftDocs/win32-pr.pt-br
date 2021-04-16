---
description: O método Notify recebe uma notificação de que uma alteração de qualidade é solicitada.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Método CBaseVideoRenderer. Notify (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750058"
---
# <a name="cbasevideorenderernotify-method"></a>Método CBaseVideoRenderer. Notify

O `Notify` método recebe uma notificação de que uma alteração de qualidade é solicitada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSelf* \[ no\]
</dt> <dd>

Ponteiro para o filtro que está enviando a notificação de qualidade.

</dd> <dt>

*q* \[ in\]
</dt> <dd>

Estrutura de notificação de qualidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) no processador de vídeo. Isso é chamado, normalmente pelo Gerenciador de gráfico de filtro, quando a qualidade deve ser recortada. Isso pode ocorrer quando a qualidade da reprodução de áudio foi aumentada para o ponto em que a qualidade da reprodução do vídeo deve ser diminuída.

`Notify` define o membro de dados **m \_ trThrottle** como um valor de atraso a ser inserido entre os quadros por [**ThrottleWait**](cbasevideorenderer-throttlewait.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




