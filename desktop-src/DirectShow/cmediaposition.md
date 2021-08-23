---
description: A classe CMediaPosition manipula os métodos IDispatch da interface dupla IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Classe CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7305d5eded589e167352ce7ff13194b52965b939daf907e8381b64684a03d1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634846"
---
# <a name="cmediaposition-class"></a>Classe CMediaPosition

![hierarquia de classe CMediaPosition](images/cutil14.png)

A classe **CMediaPosition** manipula os métodos **IDispatch** da interface dupla [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .

Essa classe herda a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , mas não a implementa. ele implementa o **IDispatch** por meio da classe [**CBaseDispatch**](cbasedispatch.md) e da biblioteca de tipos de DirectShow. Não use essa classe diretamente. Em vez disso, use uma das seguintes classes:

-   Filtros de origem: Use a classe base [**CSourceSeeking**](csourceseeking.md) para implementar a busca.
-   Filtros de transformação: Use a classe [**CPosPassThru**](cpospassthru.md) para passar comandos de busca ascendentes.
-   Renderizadores: Use a classe [**CRendererPosPassThru**](crendererpospassthru.md) para passar comandos de busca ascendentes.



| Métodos públicos                                              | Descrição                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Método de construtor.                                                                                                 |
| Métodos IDispatch                                           | Descrição                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Mapas um conjunto de nomes para um conjunto correspondente de dispids.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Recupera as informações de tipo do objeto, que podem ser usadas para obter as informações de tipo de uma interface. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo que o objeto fornece.                                            |
| [**Invoke**](cmediaposition-invoke.md)                     | Fornece acesso a propriedades e métodos expostos pelo objeto.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Classes base](directshow-base-classes.md)
</dt> </dl>

 

 




