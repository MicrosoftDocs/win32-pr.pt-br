---
description: A classe CMediaEvent fornece implementação de classe base dos métodos IDispatch da IMediaEvent de interface dupla. Ele deixa como virtual pura as propriedades e métodos da interface IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Classe CMediaEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 505a11b9a8d3c12586e25faa822b127e0b8bb636f6655eb617125a47fb84feaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832476"
---
# <a name="cmediaevent-class"></a>Classe CMediaEvent

![hierarquia de classe CMediaEvent](images/cutil03.png)

A `CMediaEvent` classe fornece a implementação de classe base dos métodos **IDispatch** do [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)de interface dual. Ele deixa como virtual pura as propriedades e métodos da interface **IMediaEvent** .

A `CMediaEvent` classe também fornece a implementação de classe base da interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) que deriva de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).

As funções de membro [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)e [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) são implementações padrão da interface **IDispatch** usando a classe [**CBaseDispatch**](cbasedispatch.md) (e uma biblioteca de tipos) para analisar os comandos e passá-los para os métodos virtuais puros da interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .



| Funções de membro                                         | Descrição                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Constrói um objeto **CMediaEvent** .                                                                                                                                                          |
| Métodos IDispatch                                        | Descrição                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Mapas um único membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que pode ser usado durante as chamadas subsequentes para o método **IDispatch:: Invoke** . |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Recupera um objeto Type-informations, que recupera as informações de tipo de uma interface.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo fornecidas por um objeto.                                                                                                                    |
| [**Invoke**](cmediaevent-invoke.md)                     | Fornece acesso a propriedades e métodos expostos por um objeto.                                                                                                                               |



 

 

 



