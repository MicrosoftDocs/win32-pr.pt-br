---
description: A classe CTransInPlaceOutputPin implementa um pino de saída que é usado pela classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Classe CTransInPlaceOutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775565"
---
# <a name="ctransinplaceoutputpin-class"></a>Classe CTransInPlaceOutputPin

![hierarquia de classe CTransInPlaceOutputPin](images/tsip02.png)

A `CTransInPlaceOutputPin` classe implementa um pino de saída que é usado pela classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Normalmente, você não precisa derivar dessa classe. Se você fizer isso, deverá substituir o método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) do filtro para criar instâncias da classe derivada.



| Variáveis de membro protegido                                                      | Descrição                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**\_pTIPFilter m**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Ponteiro para o filtro que criou este pin.         |
| Métodos públicos                                                                  | Descrição                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Método de construtor.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Determina se o PIN aceita um tipo de mídia específico. |
| [**Setalocador**](ctransinplaceoutputpin-setallocator.md)                     | Especifica um alocador para a conexão.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Recupera um ponteiro para o pino de entrada downstream.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Recupera um ponteiro para o alocador do PIN.          |
| Métodos IPin                                                                    | Descrição                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Enumera os tipos de mídia preferenciais do PIN.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




