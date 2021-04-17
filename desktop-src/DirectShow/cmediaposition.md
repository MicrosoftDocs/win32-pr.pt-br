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
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789973"
---
# <a name="cmediaposition-class"></a>Classe CMediaPosition

![hierarquia de classe CMediaPosition](images/cutil14.png)

A classe **CMediaPosition** manipula os métodos **IDispatch** da interface dupla [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .

Essa classe herda a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , mas não a implementa. Ele implementa o **IDispatch** por meio da classe [**CBaseDispatch**](cbasedispatch.md) e da biblioteca de tipos do DirectShow. Não use essa classe diretamente. Em vez disso, use uma das seguintes classes:

-   Filtros de origem: Use a classe base [**CSourceSeeking**](csourceseeking.md) para implementar a busca.
-   Filtros de transformação: Use a classe [**CPosPassThru**](cpospassthru.md) para passar comandos de busca ascendentes.
-   Renderizadores: Use a classe [**CRendererPosPassThru**](crendererpospassthru.md) para passar comandos de busca ascendentes.



| Métodos públicos                                              | Descrição                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Método de construtor.                                                                                                 |
| Métodos IDispatch                                           | Descrição                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Recupera as informações de tipo do objeto, que podem ser usadas para obter as informações de tipo de uma interface. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo que o objeto fornece.                                            |
| [**Chame**](cmediaposition-invoke.md)                     | Fornece acesso a propriedades e métodos expostos pelo objeto.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




