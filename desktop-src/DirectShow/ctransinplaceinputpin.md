---
description: A classe CTransInPlaceInputPin implementa um PIN de entrada que é usado pela classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Classe CTransInPlaceInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778440"
---
# <a name="ctransinplaceinputpin-class"></a>Classe CTransInPlaceInputPin

![hierarquia de classe CTransInPlaceInputPin](images/tsip01.png)

A `CTransInPlaceInputPin` classe implementa um PIN de entrada que é usado pela classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Normalmente, você não precisa derivar dessa classe. Se você fizer isso, deverá substituir o método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) do filtro para criar instâncias da classe derivada.



| Variáveis de membro protegido                                                          | Descrição                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_bReadOnly m**](ctransinplaceinputpin-m-breadonly.md)                           | Sinalizador que especifica se o fluxo de entrada é somente leitura. |
| [**\_pTIPFilter m**](ctransinplaceinputpin-m-ptipfilter.md)                         | Ponteiro para o filtro que criou este pin.               |
| Métodos públicos                                                                      | Descrição                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Método de construtor.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Determina se o PIN aceita um tipo de mídia específico.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Recupera um ponteiro para o alocador do PIN.                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | Indica se o fluxo de entrada é somente leitura.           |
| Métodos IPin                                                                        | Descrição                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumera os tipos de mídia preferenciais do PIN.                |
| Métodos IMemInputPin                                                                | Descrição                                                |
| [**Getalocador**](ctransinplaceinputpin-getallocator.md)                          | Recupera o alocador de memória proposto por este pin.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Especifica um alocador para a conexão.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Recupera as propriedades de alocador solicitadas pelo PIN.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




