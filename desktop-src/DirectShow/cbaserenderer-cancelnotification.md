---
description: O método CancelNotification cancela o evento de temporizador que agenda a renderização.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Método CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769241"
---
# <a name="cbaserenderercancelnotification-method"></a>Método CBaseRenderer. CancelNotification

O `CancelNotification` método cancela o evento de temporizador que agenda a renderização.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Não havia nenhum evento de timer pendente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                          |



 

## <a name="remarks"></a>Comentários

O filtro chama esse método quando o streaming é interrompido. O método cancela qualquer renderização agendada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




