---
description: A classe CEnumMediaTypes implementa um enumerador para tipos de mídia preferenciais.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Classe CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756631"
---
# <a name="cenummediatypes-class"></a>Classe CEnumMediaTypes

![hierarquia de classe CEnumMediaTypes](images/filter04.png)

A `CEnumMediaTypes` classe implementa um enumerador para tipos de mídia preferenciais.

Essa classe implementa a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . Ele chama os seguintes métodos [**CBasePin**](cbasepin.md) :

-   [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md): recupera um tipo de mídia, referenciado por um índice baseado em zero.
-   [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): determina se o conjunto de tipos preferenciais foi alterado.

Sempre que um PIN altera sua lista de tipos de mídia preferenciais, o PIN incrementa o número de versão do tipo de mídia. Quando isso acontece, o objeto enumerador não é mais sincronizado com o PIN e os métodos de classe retornam VFW \_ E \_ enum \_ fora \_ de \_ sincronia. Chame o método [**CEnumMediaTypes:: Reset**](cenummediatypes-reset.md) para ressincronizar o enumerador.



| Métodos públicos                                               | Descrição                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Método de construtor.                                             |
| [**~ CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Método destruidor. VirtuaisLUNs.                                     |
| Métodos IEnumMediaTypes                                      | Descrição                                                     |
| [**8i**](cenummediatypes-clone.md)                       | Faz uma cópia do enumerador com o mesmo estado de enumeração. |
| [**Avançar**](cenummediatypes-next.md)                         | Recupera um número especificado de tipos de mídia.                    |
| [**Redefinir**](cenummediatypes-reset.md)                       | Redefine a sequência de enumeração para o início.               |
| [**Ignorar**](cenummediatypes-skip.md)                         | Ignora um número especificado de tipos de mídia.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




