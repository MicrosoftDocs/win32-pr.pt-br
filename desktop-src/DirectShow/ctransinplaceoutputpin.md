---
description: A classe CTransInPlaceOutputPin implementa um pino de saída usado pela classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Classe CTransInPlaceOutputPin (Transip.h)
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
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076146"
---
# <a name="ctransinplaceoutputpin-class"></a>Classe CTransInPlaceOutputPin

![Hierarquia de classes ctransinplaceoutputpin](images/tsip02.png)

A `CTransInPlaceOutputPin` classe implementa um pino de saída que é usado pela classe [**CTransInPlaceFilter.**](ctransinplacefilter.md)

Normalmente, você não precisa derivar dessa classe. Se você fizer isso, deverá substituir o método [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) do filtro para criar instâncias da classe derivada.



| Variáveis de membro protegidas                                                      | Descrição                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Ponteiro para o filtro que criou esse pino.         |
| Métodos públicos                                                                  | Descrição                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Método do construtor.                                  |
| [**Checkmediatype**](ctransinplaceoutputpin-checkmediatype.md)                 | Determina se o pin aceita um tipo de mídia específico. |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | Especifica um alocador para a conexão.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Recupera um ponteiro para o pino de entrada downstream.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Recupera um ponteiro para o alocador do pino.          |
| Métodos IPin                                                                    | Descrição                                          |
| [**Enummediatypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Enumera os tipos de mídia preferenciais do pino.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




