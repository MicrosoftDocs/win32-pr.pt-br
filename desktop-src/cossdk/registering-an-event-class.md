---
description: Para que os assinantes possam encontrar uma classe de evento e assiná-la, as classes de evento devem ser registradas no catálogo COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrando uma classe de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646347"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="3a8e1-103">Registrando uma classe de evento</span><span class="sxs-lookup"><span data-stu-id="3a8e1-103">Registering an Event Class</span></span>

<span data-ttu-id="3a8e1-104">Para que os assinantes possam encontrar uma classe de evento e assiná-la, as classes de evento devem ser registradas no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="3a8e1-105">O COM+ requer uma biblioteca de tipos que descreve os métodos e as interfaces de evento para que ele possa corresponder e conectar corretamente assinantes e publicadores.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="3a8e1-106">A biblioteca de tipos deve residir ou ser acompanhada por uma DLL de registro automático.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="3a8e1-107">Você pode usar a ferramenta administrativa serviços de componentes ou as funções administrativas do COM+ para registrar uma classe de evento no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="3a8e1-108">**Para registrar uma classe de evento com a ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="3a8e1-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="3a8e1-109">Crie um novo aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="3a8e1-110">Abra a pasta do aplicativo e selecione **componentes**.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="3a8e1-111">No menu **ação** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="3a8e1-112">(Você também pode selecionar a pasta **componentes** , clique com o botão direito do mouse, aponte para **novo** e clique em **componente**.)</span><span class="sxs-lookup"><span data-stu-id="3a8e1-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="3a8e1-113">Clique em **Instalar nova classe (s) de evento**.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="3a8e1-114">Insira o caminho para a DLL de componente da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="3a8e1-115">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-115">Click **OK**.</span></span>

<span data-ttu-id="3a8e1-116">A classe de evento é registrada no catálogo COM+ e pode ser localizada por assinantes interessados em obter as informações fornecidas pela classe de evento.</span><span class="sxs-lookup"><span data-stu-id="3a8e1-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="3a8e1-117">Para obter informações sobre como registrar a classe de evento usando as interfaces administrativas do COM+, consulte [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span><span class="sxs-lookup"><span data-stu-id="3a8e1-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a8e1-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a8e1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a8e1-119">Registrando uma assinatura</span><span class="sxs-lookup"><span data-stu-id="3a8e1-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



