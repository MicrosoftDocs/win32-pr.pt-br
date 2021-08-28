---
description: Um filtro de eventos é uma classe WMI que descreve quais eventos o WMI fornece a um consumidor físico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Criando um filtro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f44f49c9a7f38b23353dc8c6343ca1d72194e3b7f121538c93f545e45c31e3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568826"
---
# <a name="creating-an-event-filter"></a>Criando um filtro de eventos

Um filtro de eventos é uma classe WMI que descreve quais eventos o WMI fornece a um consumidor físico. Por exemplo, um filtro de eventos pode instruir o WMI a fornecer a um consumidor todos os eventos de gerenciamento de energia ou todos os eventos de reinicialização do sistema. Um filtro de eventos também descreve as condições sob as quais o WMI fornece os eventos. Um filtro de eventos pode especificar um evento intrínseco ou extrínsecos; e o filtro pode se referir a eventos que se originam no namespace, ou seja, que não seja o namespace do filtro. O consumidor permanente deve ter o mesmo [**CreatorSID**](--eventconsumer.md) nas instâncias de consumidor, filtro e associação. Para obter mais informações, consulte [recebendo eventos com segurança](receiving-events-securely.md).

O procedimento a seguir descreve como criar um filtro de eventos.

**Para criar um filtro de eventos**

1.  Crie uma instância da classe de sistema WMI [**\_ \_ EventFilter**](--eventfilter.md) .
2.  Crie um identificador exclusivo para o filtro com a propriedade **Name** , de uma das duas maneiras:

    -   Use um esquema privado.

        Nomear arbitrariamente os filtros de eventos funciona contanto que você não entre em conflito com outros esquemas de nomenclatura de filtro. Você deve evitar conflitos de nomenclatura porque adicionar uma instância com um valor de **nome** duplicado substitui a instância antiga.

    -   Use um GUID (identificador global exclusivo).

        Se você deixar o **nome** vazio, o WMI preencherá o **nome** com um GUID.

3.  Descreva o tipo de evento que você deseja filtrar com a propriedade de **consulta** .

    A propriedade **Query** contém a consulta linguagem WQL (WQL) que descreve o tipo de evento que você deseja filtrar. Você pode obter uma filtragem precisa usando uma variedade de operadores e extensões para WQL.

    Um evento de log do NT é gerado quando uma consulta de um consumidor de evento permanente falha. A origem do evento é WinMgmt, a ID do evento é 10 e o tipo de evento é Error.

    O WMI é mais eficiente no processamento de consultas restritivas e específicas do que consultas amplas. Ao criar uma consulta específica, você pode evitar a comunicação entre processos e o tráfego de rede desnecessários. Em casos de eventos gerados por um provedor, o WMI executa a filtragem em processo para o provedor; Isso garante que apenas os eventos que correspondem ao filtro incorrem no custo de comunicação entre processos. Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).

4.  Defina a propriedade **QueryLanguage** como o tipo de linguagem de consulta que você usa na propriedade de **consulta** .

    Você quase sempre definirá **QueryLanguage** como "WQL".

O exemplo de código a seguir descreve um filtro de evento que sinaliza um evento cada vez que o WMI cria uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) no \\ namespace raiz cimv2.

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

A propriedade **EventNamespace** especifica o namespace do qual os eventos se originam. Você não precisa criar uma instância dos filtros no namespace onde os eventos se originam. Se você não especificar o namespace, o WMI criará o filtro no namespace padrão. As classes de eventos intrínsecos, como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , estão disponíveis em todos os namespaces.

Para registrar seu consumidor lógico para notificações de eventos, você deve associar os filtros de eventos a um consumidor lógico. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

 

 



