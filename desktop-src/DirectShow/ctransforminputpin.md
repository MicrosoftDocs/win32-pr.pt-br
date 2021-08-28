---
description: A classe CTransformInputPin implementa um PIN de entrada que é usado pela classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Classe CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3df5da0ee6e80dd1da147563ef698a520222531de5cee9656ec52cb14301f66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087006"
---
# <a name="ctransforminputpin-class"></a>Classe CTransformInputPin

![hierarquia de classe CTransformInputPin](images/tfrm01.png)

A `CTransformInputPin` classe implementa um PIN de entrada que é usado pela classe [**CTransformFilter**](ctransformfilter.md) .

Normalmente, você não precisa derivar dessa classe. A maioria dos métodos nesta classe chama os métodos correspondentes na classe **CTransformFilter** , que pode ser substituída. Se você derivar dessa classe, deverá substituir o método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) do filtro para criar instâncias da classe derivada.



| Variáveis de membro protegido                                           | Descrição                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_pTransformFilter m**](ctransforminputpin-m-ptransformfilter.md) | Ponteiro para o filtro proprietário.                                                          |
| Métodos públicos                                                       | Descrição                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Método de construtor.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Determina se uma conexão de PIN é adequada.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Libera o PIN de uma conexão.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Conclui uma conexão com outro PIN.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Determina se o PIN aceita um tipo de mídia específico.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Define o tipo de mídia para a conexão.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Determina se o PIN pode aceitar amostras. VirtuaisLUNs.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Recupera o tipo de mídia para a conexão do PIN atual.                               |
| Métodos IPin                                                         | Descrição                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Recupera um identificador para o PIN.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Notifica o PIN de que nenhum dado adicional é esperado.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Inicia uma operação de liberação.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Finaliza uma operação de liberação.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Notifica o PIN que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento. |
| Métodos IMemInputPin                                                 | Descrição                                                                            |
| [**Recebe**](ctransforminputpin-receive.md)                        | Recebe o próximo exemplo de mídia no fluxo.                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




