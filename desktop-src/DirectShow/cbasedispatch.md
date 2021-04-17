---
description: A classe CBaseDispatch é uma classe base para implementar a interface IDispatch em um filtro do DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Classe CBaseDispatch (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748833"
---
# <a name="cbasedispatch-class"></a>Classe CBaseDispatch

![hierarquia de classe CBaseDispatch](images/cutil01.png)

A classe **CBaseDispatch** é uma classe base para implementar a interface **IDispatch** em um filtro do DirectShow.

Essa classe é limitada ao suporte às interfaces compatíveis com automação exportadas pela biblioteca de tipos do DirectShow, QuartzTypeLib. Por exemplo, as classes [**CMediaControl**](cmediacontrol.md) e [**CMediaPosition**](cmediaposition.md) usam **CBaseDispatch** para implementar [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectivamente. Devido a essa limitação, provavelmente não há motivo para usar o **CBaseDispatch** diretamente em seus próprios filtros.

Para usar essa classe, faça o seguinte:

-   Declare uma nova classe que dê suporte a **IDispatch**.
-   Dê à sua nova classe uma variável de membro privado do tipo **CBaseDispatch**.
-   Implemente os métodos **IDispatch** .
-   Em seus métodos **IDispatch** , chame os métodos **CBaseDispatch** .

Para obter mais detalhes, consulte o código-fonte de qualquer uma das classes de exemplo declaradas em Ctlutil. h.



| Métodos públicos                                             | Descrição                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Método de construtor.                                                                                                 |
| [**~ CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Método destruidor.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Recupera as informações de tipo do objeto, que podem ser usadas para obter as informações de tipo de uma interface. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo que o objeto fornece.                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




