---
description: A classe CTransformOutputPin implementa um pino de saída que é usado pela classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Classe CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758650"
---
# <a name="ctransformoutputpin-class"></a>Classe CTransformOutputPin

![hierarquia de classe CTransformOutputPin](images/tfrm02.png)

A `CTransformOutputPin` classe implementa um pino de saída que é usado pela classe [**CTransformFilter**](ctransformfilter.md) .

Normalmente, você não precisa derivar dessa classe. A maioria dos métodos nesta classe chama os métodos correspondentes na classe **CTransformFilter** , que pode ser substituída. Se você derivar dessa classe, deverá substituir o método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) do filtro para criar instâncias da classe derivada.

Essa classe expõe as interfaces **IMediaSeeking** e **IMediaPosition** por meio do objeto [**CPosPassThru**](cpospassthru.md) . Ele passa todas as solicitações de busca para o próximo filtro upstream.



| Variáveis de membro protegido                                               | Descrição                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**\_pTransformFilter m**](ctransformoutputpin-m-ptransformfilter.md)    | Ponteiro para o filtro proprietário.                            |
| Variáveis de membro público                                                  | Descrição                                              |
| [**\_pPosition m**](ctransformoutputpin-m-pposition.md)                  | Objeto auxiliar para passar comandos de busca upstream.            |
| Métodos públicos                                                           | Descrição                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Método de construtor.                                      |
| [**~ CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Método destruidor.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Determina se uma conexão de PIN é adequada.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Libera o PIN de uma conexão.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Conclui uma conexão com outro PIN.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Determina se o PIN aceita um tipo de mídia específico.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Define o tipo de mídia para a conexão.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Define os requisitos de buffer.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Recupera um tipo de mídia preferencial, por valor de índice.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Recupera o tipo de mídia para a conexão do PIN atual. |
| Métodos IPin                                                             | Descrição                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Recupera um identificador para o PIN.                     |
| Métodos IQualityControl                                                  | Descrição                                              |
| [**Notificar**](ctransformoutputpin-notify.md)                             | Notifica o PIN de que uma alteração de qualidade é solicitada.     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




