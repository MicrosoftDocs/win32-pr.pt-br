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
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="05e6f-104">Registrando uma assinatura transitória</span><span class="sxs-lookup"><span data-stu-id="05e6f-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="05e6f-105">Assinaturas transitórias solicitam um evento para um objeto de Assinante específico que já existe.</span><span class="sxs-lookup"><span data-stu-id="05e6f-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="05e6f-106">As assinaturas transitórias são armazenadas no catálogo COM+, mas a assinatura é excluída se o sistema de eventos ou o sistema operacional for interrompido.</span><span class="sxs-lookup"><span data-stu-id="05e6f-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="05e6f-107">Ao contrário das assinaturas persistentes, as assinaturas transitórias são vinculadas a um objeto específico e são armazenadas apenas no sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="05e6f-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="05e6f-108">Se houver um problema com o sistema de eventos ou sistema operacional, a assinatura desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="05e6f-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="05e6f-109">Assinaturas transitórias podem ser mais eficientes do que assinaturas persistentes, mas você deve gerenciar seus ciclos de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="05e6f-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="05e6f-110">Não é possível definir assinaturas transitórias usando a ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="05e6f-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="05e6f-111">Você deve usar as interfaces administrativas do COM+ para criar ou atualizar uma assinatura transitória.</span><span class="sxs-lookup"><span data-stu-id="05e6f-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="05e6f-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="05e6f-112">Visual Basic</span></span>

<span data-ttu-id="05e6f-113">O procedimento a seguir descreve como criar uma assinatura transitória usando o Microsoft Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="05e6f-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="05e6f-114">Especifique uma assinatura como transitória adicionando uma nova entrada à coleção [**TransientSubscriptions**](transientsubscriptions.md) e definindo a propriedade SubscriberInterface como a interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) do objeto Subscriber.</span><span class="sxs-lookup"><span data-stu-id="05e6f-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="05e6f-115">Os eventos COM+ não criam uma nova instância do objeto de assinante ao acionar um evento, mas sim usa a instância que você especificar.</span><span class="sxs-lookup"><span data-stu-id="05e6f-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="05e6f-116">Os eventos COM+ contêm uma contagem de referência para o objeto de assinante até que a assinatura seja removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="05e6f-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="05e6f-117">Crie um aplicativo de servidor COM+ (um. exe, um. dll ou um arquivo. ocx) com um objeto que implementa as interfaces ou os métodos que você deseja assinar.</span><span class="sxs-lookup"><span data-stu-id="05e6f-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="05e6f-118">Crie sua assinatura transitória usando o código a seguir, passando o CLSID do objeto de [classe de evento](the-com--event-class-object.md) e a instância do objeto de assinante.</span><span class="sxs-lookup"><span data-stu-id="05e6f-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="05e6f-119">Usando a ferramenta administrativa serviços de componentes, você pode obter a propriedade EventCLSID clicando com o botão direito do mouse no componente COM+, selecionando **Propriedades** e selecionando a guia **geral** .</span><span class="sxs-lookup"><span data-stu-id="05e6f-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

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

<span data-ttu-id="05e6f-120">O exemplo a seguir ilustra como chamar a função CreateTransientSubscription para assinar uma interface chamada IStockTicker, que tem um método chamado UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="05e6f-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="05e6f-121">Crie uma classe de evento que dê suporte à interface IStockTicker, que tem um método, UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="05e6f-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="05e6f-122">No projeto do Assinante, adicione uma classe que implemente a interface IStockTicker.</span><span class="sxs-lookup"><span data-stu-id="05e6f-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="05e6f-123">Quando você quiser assinar, execute o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="05e6f-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="05e6f-124">A função CreateTransientSubscription retorna uma cadeia de caracteres, que é um GUID que pode ser usado como um identificador ou um cookie para revogar a assinatura mais tarde.</span><span class="sxs-lookup"><span data-stu-id="05e6f-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="05e6f-125">Para remover a assinatura, chame o método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) na coleção [**TransientSubscriptions**](transientsubscriptions.md) , passando o índice correspondente à assinatura com o GUID recebido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05e6f-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05e6f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05e6f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05e6f-127">Registrando uma assinatura</span><span class="sxs-lookup"><span data-stu-id="05e6f-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
