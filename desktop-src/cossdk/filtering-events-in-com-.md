---
description: 'Os eventos COM+ fornecem duas maneiras de controlar quais eventos atingem quais assinantes: filtragem de Publicador e filtragem de parâmetros.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrando eventos no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646490"
---
# <a name="filtering-events-in-com"></a>Filtrando eventos no COM+

Os eventos COM+ fornecem duas maneiras de controlar quais eventos atingem quais assinantes: *filtragem de Publicador* e *filtragem de parâmetros*.

## <a name="publisher-filtering"></a>Filtragem de Publicador

A filtragem de Publicador controla a ordem e o acionamento de um método de evento por um objeto de [classe de evento](the-com--event-class-object.md) . A filtragem de Publicador permite que o Publicador determine quais assinantes recebem um evento específico.

Um exemplo de uso efetivo da filtragem de Publicador é o de uma troca de estoque. A maioria dos assinantes deseja saber quando uma nova ação é adicionada. No entanto, muitos desses mesmos assinantes talvez não queiram saber sempre que cada preço de estoque é alterado. A filtragem de Publicador fornece a granularidade necessária para entregar com eficiência os eventos apenas aos assinantes que desejam essas informações.

Quando um método é invocado no objeto da classe de evento instanciado, ele coleta todos os filtros do editor nesse método. O filtro força o objeto de evento a acionar o método de evento para um Assinante específico. O filtro determina quais assinaturas são acionadas e em qual ordem para disfire-las. Por exemplo, o filtro pode ler a lista de assinaturas e criar a ordem com base em alguns critérios de aplicativo e, em seguida, chamar os assinantes nessa ordem.

Para obter instruções detalhadas sobre como criar um filtro de Publicador, consulte [criando um filtro de Publicador](creating-a-publisher-filter.md).

## <a name="parameter-filtering"></a>Filtragem de parâmetro

Ao contrário da filtragem de Publicador, o serviço de eventos COM+ fornece uma filtragem de parâmetro de assinante opcional para cada assinatura e cada invocação de método de evento. A filtragem de parâmetro avalia a propriedade FilterCriteria da assinatura em relação aos parâmetros do método de evento. Esse tipo de filtragem é usado em uma base por cada assinatura e fornece um nível de filtragem de Assinante na origem do evento. A cadeia de caracteres de critérios de filtro reconhece os operadores relacionais para verificar a igualdade (=, = =,!,! =, ~, ~ =,  <>), parênteses aninhados e palavras-chave lógicas **e**, **ou**, ou **não**.

A filtragem de parâmetro ocorre depois de qualquer filtragem de Publicador e quando o objeto de evento padrão é acionado para uma determinada assinatura. Se a filtragem de Publicador for usada, a filtragem de parâmetros ocorrerá somente quando o filtro de editor invocar [**IFiringControl:: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription). Por isso, a filtragem de editores e a filtragem de parâmetros podem compor juntas, mas a filtragem de Publicador tem precedência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Publicando e fornecendo eventos no COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Assinaturas](subscriptions.md)
</dt> <dt>

[O objeto de classe de evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Usando eventos COM+ com componentes em fila COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



