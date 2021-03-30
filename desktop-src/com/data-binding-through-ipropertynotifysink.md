---
title: Vinculação de dados por meio de IPropertyNotifySink
description: Vinculação de dados por meio de IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d39c7277d27f0df6c185fc35a926aa98b77b91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637156"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Vinculação de dados por meio de IPropertyNotifySink

Os objetos que dão suporte a propriedades, por exemplo, por meio da automação OLE e da interface **IDispatch** , podem querer permitir que os clientes sejam notificados quando determinadas propriedades alteram o valor. Essa propriedade é chamada de propriedade vinculável porque as notificações permitem que um cliente sincronize sua própria exibição dos valores de propriedade atuais do objeto. Além disso, os mesmos objetos talvez queiram permitir que um cliente controle quando determinadas propriedades têm permissão para serem alteradas. Essas propriedades são chamadas de propriedades de edição de solicitação.

O [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) é uma interface de notificação padrão que dá suporte às propriedades bindable e Request-Edit. **IPropertyNotifySink** tem suporte de um objeto com propriedades como uma interface de saída. Ou seja, a própria interface é implementada pelo objeto de coletor de um cliente e o cliente conecta o coletor ao objeto de suporte por meio do mecanismo de ponto de conexão descrito anteriormente. O **IPropertyNotifySink** é definido da seguinte maneira:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Quando um objeto deseja notificar seus coletores conectados de que uma propriedade vinculável identificada com um determinado DISPID foi alterado, ele chama [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Se um objeto alterar várias propriedades de uma só vez, ele poderá passar DISPID \_ Unknown para **OnChanged** , caso em que um cliente atualiza seu cache de todos os valores de propriedade de interesse.

Quando uma propriedade de edição de solicitação está prestes a ser alterada, um objeto pode perguntar ao cliente se ele permitirá que essa alteração ocorra. O objeto chama [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) passando o DispID da propriedade em questão (ou DISPID \_ desconhecido para identificar todas as propriedades). O coletor do cliente retorna S \_ OK para indicar que a alteração é permitida ou s \_ false (ou um erro) para indicar que a alteração não é permitida. Quando um objeto chama **OnRequestEdit**, é necessário obedecer aos desejos do cliente seguindo a semântica exata dos \_ valores de retorno S OK e s \_ falsos.

Observe que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) não pode ser usado para validação de dados porque, no momento da chamada, o novo valor da propriedade ainda não está disponível. A notificação só pode ser usada para controlar um estado somente leitura para uma propriedade.

Objetos controlam quais propriedades são vinculáveis e solicitam editar e marcar essas propriedades nas informações de tipo do objeto. Nas informações de tipo, o atributo ligável marca uma propriedade como suporte [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). O atributo requestedit marca uma propriedade como [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit)de suporte.

Uma propriedade pode dar suporte a ambos os comportamentos, caso em que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) é chamado primeiro, e somente se a alteração for permitida for [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) chamada.

A única exceção ao comportamento dessas propriedades é que nenhuma notificação é enviada como resultado dos procedimentos de inicialização ou carregamento de um objeto. Nesses momentos, supõe-se que todas as propriedades sejam alteradas e que todas devem ter permissão para serem alteradas. As notificações para essa interface são, portanto, apenas significativas no contexto de um objeto totalmente inicializado/carregado.

Dois outros atributos podem ser aplicados às propriedades nas informações de tipo de um objeto. O atributo defaultbind marca uma propriedade vinculável como sendo a que melhor representa o estado do objeto como um todo. O atributo displaybind marca uma propriedade vinculável como adequada para exibição na interface do usuário de um cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




