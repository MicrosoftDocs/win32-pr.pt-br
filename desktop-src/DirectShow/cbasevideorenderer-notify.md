---
description: O método Notify recebe uma notificação de que uma alteração de qualidade é solicitada.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Método CBaseVideoRenderer.Notify (Renbase.h)
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
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052186"
---
# <a name="cbasevideorenderernotify-method"></a>Método CBaseVideoRenderer.Notify

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

*pSelf* \[ Em\]
</dt> <dd>

Ponteiro para o filtro que está enviando a notificação de qualidade.

</dd> <dt>

*q* \[ em\]
</dt> <dd>

Estrutura de notificação de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro implementa o [**método IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) no renderador de vídeo. Isso é chamado, normalmente pelo gerenciador de grafo de filtro, quando a qualidade deve ser recortada. Isso pode ocorrer quando a qualidade da reprodução de áudio foi aumentada até o ponto em que a qualidade da reprodução de vídeo deve ser reduzida.

`Notify` define o **membro de dados m \_ trThrottle** como um valor de atraso a ser inserido entre quadros por [**ThrottleWait**](cbasevideorenderer-throttlewait.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




