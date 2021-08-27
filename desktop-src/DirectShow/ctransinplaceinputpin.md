---
description: A classe CTransInPlaceInputPin implementa um pino de entrada usado pela classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Classe CTransInPlaceInputPin (Transip.h)
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
ms.openlocfilehash: 04d30b18d115e7ef03e88deb47355bafc795532a91afa14cf2f4392e658954f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076187"
---
# <a name="ctransinplaceinputpin-class"></a>Classe CTransInPlaceInputPin

![Hierarquia de classes ctransinplaceinputpin](images/tsip01.png)

A `CTransInPlaceInputPin` classe implementa um pino de entrada que é usado pela classe [**CTransInPlaceFilter.**](ctransinplacefilter.md)

Normalmente, você não precisa derivar dessa classe. Se você fizer isso, deverá substituir o método [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) do filtro para criar instâncias da classe derivada.



| Variáveis de membro protegidas                                                          | Descrição                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | Sinalizador que especifica se o fluxo de entrada é somente leitura. |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Ponteiro para o filtro que criou esse pino.               |
| Métodos públicos                                                                      | Descrição                                                |
| [**Ctransinplaceinputpin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Método do construtor.                                        |
| [**Checkmediatype**](ctransinplaceinputpin-checkmediatype.md)                      | Determina se o pin aceita um tipo de mídia específico.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Recupera um ponteiro para o alocador do pino.                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | Indica se o fluxo de entrada é somente leitura.           |
| Métodos IPin                                                                        | Descrição                                                |
| [**Enummediatypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumera os tipos de mídia preferenciais do pino.                |
| Métodos IMemInputPin                                                                | Descrição                                                |
| [**Getallocator**](ctransinplaceinputpin-getallocator.md)                          | Recupera o alocador de memória proposto por esse pino.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Especifica um alocador para a conexão.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Recupera as propriedades do alocador solicitadas pelo pino.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




