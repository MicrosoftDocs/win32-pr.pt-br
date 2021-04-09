---
description: Não é possível definir assinaturas transitórias usando a ferramenta de administração de serviços de componentes. Você deve usar as interfaces administrativas do COM+ para criar ou atualizar uma assinatura transitória.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrando uma assinatura transitória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089173"
---
# <a name="registering-a-transient-subscription"></a>Registrando uma assinatura transitória

Assinaturas transitórias solicitam um evento para um objeto de Assinante específico que já existe. As assinaturas transitórias são armazenadas no catálogo COM+, mas a assinatura é excluída se o sistema de eventos ou o sistema operacional for interrompido. Ao contrário das assinaturas persistentes, as assinaturas transitórias são vinculadas a um objeto específico e são armazenadas apenas no sistema de eventos. Se houver um problema com o sistema de eventos ou sistema operacional, a assinatura desaparecerá. Assinaturas transitórias podem ser mais eficientes do que assinaturas persistentes, mas você deve gerenciar seus ciclos de vida do objeto.

Não é possível definir assinaturas transitórias usando a ferramenta de administração de serviços de componentes. Você deve usar as interfaces administrativas do COM+ para criar ou atualizar uma assinatura transitória.

## <a name="visual-basic"></a>Visual Basic

O procedimento a seguir descreve como criar uma assinatura transitória usando o Microsoft Visual Basic:

1.  Especifique uma assinatura como transitória adicionando uma nova entrada à coleção [**TransientSubscriptions**](transientsubscriptions.md) e definindo a propriedade SubscriberInterface como a interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) do objeto Subscriber. Os eventos COM+ não criam uma nova instância do objeto de assinante ao acionar um evento, mas sim usa a instância que você especificar. Os eventos COM+ contêm uma contagem de referência para o objeto de assinante até que a assinatura seja removida do sistema.
2.  Crie um aplicativo de servidor COM+ (um. exe, um. dll ou um arquivo. ocx) com um objeto que implementa as interfaces ou os métodos que você deseja assinar.
3.  Crie sua assinatura transitória usando o código a seguir, passando o CLSID do objeto de [classe de evento](the-com--event-class-object.md) e a instância do objeto de assinante. Usando a ferramenta administrativa serviços de componentes, você pode obter a propriedade EventCLSID clicando com o botão direito do mouse no componente COM+, selecionando **Propriedades** e selecionando a guia **geral** .

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

O exemplo a seguir ilustra como chamar a função CreateTransientSubscription para assinar uma interface chamada IStockTicker, que tem um método chamado UpdateStock.

1.  Crie uma classe de evento que dê suporte à interface IStockTicker, que tem um método, UpdateStock.
2.  No projeto do Assinante, adicione uma classe que implemente a interface IStockTicker.
3.  Quando você quiser assinar, execute o seguinte código:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

A função CreateTransientSubscription retorna uma cadeia de caracteres, que é um GUID que pode ser usado como um identificador ou um cookie para revogar a assinatura mais tarde. Para remover a assinatura, chame o método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) na coleção [**TransientSubscriptions**](transientsubscriptions.md) , passando o índice correspondente à assinatura com o GUID recebido anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando uma assinatura](registering-a-subscription.md)
</dt> </dl>

 

 
