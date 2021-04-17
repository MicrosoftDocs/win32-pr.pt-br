---
description: O método Stop interrompe o filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Método CBaseRenderer. Stop (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748214"
---
# <a name="cbaserendererstop-method"></a>Método CBaseRenderer. Stop

O `Stop` método para o filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseFilter:: Stop**](cbasefilter-stop.md) . Ele executa as seguintes ações:

-   Chama [**CBaseFilter:: Stop**](cbasefilter-stop.md).
-   O desconfirma o alocador. (Consulte [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)
-   Cancela qualquer renderização agendada e libera o thread de streaming.
-   Aguarda a conclusão de qualquer chamada de **recebimento** pendente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




