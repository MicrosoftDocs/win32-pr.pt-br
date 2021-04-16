---
description: A classe CEnumPins implementa um enumerador para Pins.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Classe CEnumPins (Amfilter. h)
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
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751245"
---
# <a name="cenumpins-class"></a>Classe CEnumPins

![hierarquia de classe CEnumPins](images/filter03.png)

A `CEnumPins` classe implementa um enumerador para Pins.

Essa classe implementa a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . Ele chama os seguintes métodos [**CBaseFilter**](cbasefilter.md) :

-   [**CBaseFilter:: GetPin**](cbasefilter-getpin.md): recupera um PIN no filtro, referenciado por um índice baseado em zero.
-   [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md): recupera o número total de Pins no filtro.
-   [**CBaseFilter:: GetPinVersion**](cbasefilter-getpinversion.md): determina se os Pins foram alterados.

Se o filtro cria ou destrói Pins dinamicamente, ele incrementa a versão do PIN sempre que os Pins são alterados. Se o número de versão for alterado, o objeto enumerador não será mais sincronizado com o filtro. Depois que o enumerador estiver fora de sincronia, os métodos em `CEnumPins` retornarão VFW \_ E \_ enum \_ fora \_ de \_ sincronia. Chame o método [**CEnumPins:: Reset**](cenumpins-reset.md) para ressincronizar o enumerador.



| Métodos públicos                             | Descrição                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Método de construtor.                                             |
| [**~ CEnumPins**](cenumpins--cenumpins.md) | Método destruidor. VirtuaisLUNs.                                     |
| Métodos IEnumPins                          | Descrição                                                     |
| [**8i**](cenumpins-clone.md)           | Faz uma cópia do enumerador com o mesmo estado de enumeração. |
| [**Avançar**](cenumpins-next.md)             | Recupera um número especificado de Pins.                           |
| [**Redefinir**](cenumpins-reset.md)           | Redefine a sequência de enumeração para o início.               |
| [**Ignorar**](cenumpins-skip.md)             | Ignora um número especificado de Pins.                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




