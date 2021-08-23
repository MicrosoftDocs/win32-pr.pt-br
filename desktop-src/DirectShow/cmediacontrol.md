---
description: A classe CMediaControl fornece a manipulação de classe base dos métodos IDispatch da IMediaControl de interface dupla. Ele deixa como virtual pura as propriedades e métodos da Interface IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Classe CMediaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: 119ffb93cb307db1da3bc8c7562851d63c5f9eeb8e0e3b80be62c8110181c32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074070"
---
# <a name="cmediacontrol-class"></a>Classe CMediaControl

![hierarquia de classe CMediaControl](images/cutil02.png)

A `CMediaControl` classe fornece a manipulação de classe base dos métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) do [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)de interface dupla. Ele deixa como virtual pura as propriedades e métodos da interface **IMediaControl** .

Normalmente, o Gerenciador do grafo de filtro é o único objeto que implementa a interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) . (os filtros implementam a interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , herdada por [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), para receber comandos de controle do Gerenciador de gráfico de filtro.) Portanto, essa biblioteca de classes é de uso limitado para filtrar os desenvolvedores.

As funções de membro [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)e [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) são implementações padrão dos métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) usando a classe [**CBaseDispatch**](cbasedispatch.md) (e uma biblioteca de tipos) para analisar os comandos e passá-los para os métodos virtuais puros da interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .

Os métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , definidos em Control. ODL, são deixados como virtuais puros.



| Funções de membro                                           | Descrição                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Constrói um objeto **CMediaControl** .                                                                                                                                                                                                  |
| Métodos IDispatch                                          | Descrição                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Mapas um único membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro (dispids), que pode ser usado durante as chamadas subsequentes para o método [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) . |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Recupera o número de interfaces de informações de tipo fornecidas por um objeto.                                                                                                                                                              |
| [**Invoke**](cmediacontrol-invoke.md)                     | Fornece acesso a propriedades e métodos expostos por um objeto.                                                                                                                                                                         |



 

 

 
