---
description: Depois de registrar uma classe de evento no catálogo COM+, você pode adicionar assinantes à classe de evento e assinaturas aos assinantes.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrando uma assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370478"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="f21f6-103">Registrando uma assinatura</span><span class="sxs-lookup"><span data-stu-id="f21f6-103">Registering a Subscription</span></span>

<span data-ttu-id="f21f6-104">Depois de registrar uma classe de evento no catálogo COM+, você pode adicionar assinantes à classe de evento e assinaturas aos assinantes.</span><span class="sxs-lookup"><span data-stu-id="f21f6-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="f21f6-105">As assinaturas podem assinar um único método ou todos os métodos de uma interface.</span><span class="sxs-lookup"><span data-stu-id="f21f6-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="f21f6-106">Para receber chamadas em mais de um método — mas não em todos os métodos — de uma interface, você deve adicionar uma assinatura para cada método para o qual deseja receber uma chamada.</span><span class="sxs-lookup"><span data-stu-id="f21f6-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="f21f6-107">A ferramenta de administração de serviços de componentes pode pesquisar classes de evento registradas no catálogo COM+ que dão suporte às interfaces implementadas pelo assinante e oferece a opção de assinar.</span><span class="sxs-lookup"><span data-stu-id="f21f6-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="f21f6-108">Escolha o Publicador que oferece os eventos desejados.</span><span class="sxs-lookup"><span data-stu-id="f21f6-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="f21f6-109">Para adicionar assinantes ao componente assinante, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="f21f6-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="f21f6-110">Depois de criar um novo aplicativo COM+ e instalar o componente de assinante, clique com o botão direito do mouse na pasta **assinaturas** para habilitar o assistente de nova assinatura do com+.</span><span class="sxs-lookup"><span data-stu-id="f21f6-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="f21f6-111">Escolha a classe de evento da qual você deseja receber eventos.</span><span class="sxs-lookup"><span data-stu-id="f21f6-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="f21f6-112">Insira um nome para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="f21f6-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="f21f6-113">Habilite a assinatura.</span><span class="sxs-lookup"><span data-stu-id="f21f6-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="f21f6-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f21f6-114">Click **OK**.</span></span>

<span data-ttu-id="f21f6-115">Quando um aplicativo do Publicador deseja acionar um evento, o Publicador instancia o objeto da classe de evento e chama um método nele.</span><span class="sxs-lookup"><span data-stu-id="f21f6-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="f21f6-116">O COM+ pesquisa o catálogo COM+ para localizar todos os assinantes.</span><span class="sxs-lookup"><span data-stu-id="f21f6-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="f21f6-117">Ele cria o objeto de assinante (diretamente, na fila ou com um moniker) e passa a chamada de método originalmente feita pelo Publicador.</span><span class="sxs-lookup"><span data-stu-id="f21f6-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f21f6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f21f6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f21f6-119">Registrando uma classe de evento</span><span class="sxs-lookup"><span data-stu-id="f21f6-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



