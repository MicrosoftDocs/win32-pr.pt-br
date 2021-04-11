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
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172512"
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
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Mapeia um único membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que podem ser usados durante as chamadas subsequentes para o método **IDispatch:: Invoke** . |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Recupera um objeto Type-informations, que recupera as informações de tipo de uma interface.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo fornecidas por um objeto.                                                                                                                    |
| [**Chame**](cmediaevent-invoke.md)                     | Fornece acesso a propriedades e métodos expostos por um objeto.                                                                                                                               |



 

 

 



