---
description: A classe CEnumPins implementa um enumerador para pinos.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Classe CEnumPins (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7135a07aedb879503d36011b274bdeab8035924b91bb5d9bc656d6d89dfbe201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566996"
---
# <a name="cenumpins-class"></a>Classe CEnumPins

![Hierarquia de classes cenumpins](images/filter03.png)

A `CEnumPins` classe implementa um enumerador para pinos.

Essa classe implementa a interface [**IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) Ele chama os seguintes [**métodos CBaseFilter:**](cbasefilter.md)

-   [**CBaseFilter::GetPin:**](cbasefilter-getpin.md)recupera um pino no filtro, referenciado por um índice baseado em zero.
-   [**CBaseFilter::GetPinCount:**](cbasefilter-getpincount.md)recupera o número total de pinos no filtro.
-   [**CBaseFilter::GetPinVersion:**](cbasefilter-getpinversion.md)determina se os pinos foram alterados.

Se o filtro criar ou destruir pinos dinamicamente, ele incrementa a versão do pino sempre que os pinos mudam. Se o número de versão mudar, o objeto enumerador não será mais sincronizado com o filtro. Quando o enumerador está fora de sincronia, os métodos em `CEnumPins` retornam VFW \_ \_ ENUM \_ OUT OF \_ \_ SYNC. Chame o [**método CEnumPins::Reset**](cenumpins-reset.md) para ressincronizar o enumerador.



| Métodos públicos                             | Descrição                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**Cenumpins**](cenumpins-cenumpins.md)   | Método do construtor.                                             |
| [**~CEnumPins**](cenumpins--cenumpins.md) | Método destruidor. Virtual.                                     |
| Métodos IEnumPins                          | Descrição                                                     |
| [**Clone**](cenumpins-clone.md)           | Faz uma cópia do enumerador com o mesmo estado de enumeração. |
| [**Avançar**](cenumpins-next.md)             | Recupera um número especificado de pinos.                           |
| [**Redefinir**](cenumpins-reset.md)           | Redefine a sequência de enumeração para o início.               |
| [**Ignorar**](cenumpins-skip.md)             | Ignora um número especificado de pinos.                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




