---
description: A classe CBaseDispatch é uma classe base para implementar a interface IDispatch em um DirectShow filtro.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Classe CBaseDispatch (Ctlutil.h)
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
ms.openlocfilehash: 1a094ad3b79dbeb8c4dfc2888de01a521738740fc19ad70b521172d3194fd9f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793307"
---
# <a name="cbasedispatch-class"></a>Classe CBaseDispatch

![Hierarquia de classes cbasedispatch](images/cutil01.png)

A **classe CBaseDispatch** é uma classe base para implementar a interface **IDispatch** em um DirectShow filtro.

Essa classe está limitada a dar suporte às interfaces compatíveis com a Automação exportadas pela biblioteca de tipos DirectShow, DigitTypeLib. Por exemplo, as [**classes CMediaControl**](cmediacontrol.md) e [**CMediaPosition**](cmediaposition.md) usam **CBaseDispatch** para implementar [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition)respectivamente. Devido a essa limitação, provavelmente não há motivo para usar **CBaseDispatch** diretamente em seus próprios filtros.

Para usar essa classe, faça o seguinte:

-   Declare uma nova classe que dá suporte **a IDispatch.**
-   Dê à nova classe uma variável de membro privado do **tipo CBaseDispatch.**
-   Implemente **os métodos IDispatch.**
-   Em seus **métodos IDispatch,** chame os **métodos CBaseDispatch.**

Para obter mais detalhes, consulte o código-fonte para qualquer uma das classes de exemplo declaradas em Ctlutil.h.



| Métodos públicos                                             | Descrição                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Cbasedispatch**](cbasedispatch-cbasedispatch.md)       | Método do construtor.                                                                                                 |
| [**~CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Método destruidor.                                                                                                  |
| [**Getidsofnames**](cbasedispatch-getidsofnames.md)       | Mapas um conjunto de nomes para um conjunto correspondente de DISPIDs.                                                              |
| [**Gettypeinfo**](cbasedispatch-gettypeinfo.md)           | Recupera as informações de tipo do objeto , que podem ser usadas para obter as informações de tipo de uma interface. |
| [**Gettypeinfocount**](cbasedispatch-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo que o objeto fornece.                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Base Classes](directshow-base-classes.md)
</dt> </dl>

 

 




