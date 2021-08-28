---
title: Vinculação de dados por meio de IPropertyNotifySink
description: Vinculação de dados por meio de IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337233455872928f824d8cbb903aba247b1ef496d02c0af04223361731fe3663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854646"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Vinculação de dados por meio de IPropertyNotifySink

Objetos que suportam propriedades, por exemplo, por meio da Automação OLE e da interface **IDispatch,** podem querer permitir que os clientes sejam notificados quando determinadas propriedades alterarem o valor. Essa propriedade é chamada de propriedade a vincável porque as notificações permitem que um cliente sincronizar sua própria exibição dos valores de propriedade atuais do objeto. Além disso, os mesmos objetos podem querer permitir que um cliente controle quando determinadas propriedades têm permissão para alterar. Essas propriedades são chamadas de propriedades de edição de solicitação.

O [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) é uma interface de notificação padrão que dá suporte a propriedades a bindable e request-edit. **Há suporte para IPropertyNotifySink** em um objeto com propriedades como uma interface de saída. Ou seja, a própria interface é implementada pelo objeto de sink de um cliente e o cliente conecta o sink ao objeto de suporte por meio do mecanismo de ponto de conexão descrito anteriormente. O **IPropertyNotifySink** é definido da seguinte forma:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Quando um objeto deseja notificar seus sinks conectados de que uma propriedade a vinciável identificada com um determinado DISPID foi alterada, ele chama [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Se um objeto altera várias propriedades de uma só vez, ele pode passar DISPID UNKNOWN para \_ **OnChanged,** caso em que um cliente atualiza seu cache de todos os valores de propriedade de interesse.

Quando uma propriedade de edição de solicitação está prestes a mudar, um objeto pode perguntar ao cliente se ela permitirá que essa alteração ocorra. O objeto chama [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) passando o DISPID da propriedade em questão (ou DISPID \_ UNKNOWN para identificar todas as propriedades). O sink do cliente retorna S OK para indicar que a alteração é permitida ou S FALSE (ou um erro) para indicar que a alteração \_ \_ não é permitida. Quando um objeto chama **OnRequestEdit**, é necessário obedecer aos desejos do cliente seguindo a semântica exata dos valores de retorno S OK e \_ S \_ FALSE.

Observe que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) não pode ser usado para validação de dados porque, no momento da chamada, o novo valor da propriedade ainda não está disponível. A notificação só pode ser usada para controlar um estado somente leitura para uma propriedade.

Os objetos controlam quais propriedades são a bindáveis e solicitam a edição e marcam essas propriedades nas informações de tipo do objeto. Nas informações de tipo, o atributo a vinciável marca uma propriedade como dando suporte [**a OnChanged.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) O atributo requestedit marca uma propriedade como dando suporte [**a OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit).

Uma propriedade pode dar suporte a ambos os comportamentos, caso em que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) é chamado primeiro e somente se a alteração for permitida [**é OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) chamado.

A única exceção ao comportamento dessas propriedades é que nenhuma notificação é enviada como resultado dos procedimentos de inicialização ou carregamento de um objeto. Nesses momentos, supõe-se que todas as propriedades sejam alteradas e que todas devem ter permissão para alterar. As notificações para essa interface são, portanto, significativas apenas no contexto de um objeto totalmente inicializado/carregado.

Dois outros atributos podem ser aplicados às propriedades nas informações de tipo de um objeto. O atributo defaultbind marca uma propriedade a vincável como sendo aquela que melhor representa o estado do objeto como um todo. O atributo displaybind marca uma propriedade a vincável como adequada para exibição na própria interface do usuário do cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




