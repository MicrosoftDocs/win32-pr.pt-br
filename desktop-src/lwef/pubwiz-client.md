---
title: Design de Client-Side
description: O script em páginas HTML do lado do servidor se comunica com o cliente do assistente de ordenação de impressão online no qual ele está hospedado. Essa comunicação é realizada por meio de métodos e propriedades acessados pelo objeto Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- assistentes de publicação, design do lado do cliente
- janela. external, assistentes de publicação
- assistentes de publicação, janela. externa
- assistentes de publicação, considerações de design
- assistentes de publicação, assistente para ordenação de impressão online
- Assistente de ordenação de impressão online, design do lado do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917280"
---
# <a name="client-side-design"></a><span data-ttu-id="eeb39-110">Design de Client-Side</span><span class="sxs-lookup"><span data-stu-id="eeb39-110">Client-Side Design</span></span>

<span data-ttu-id="eeb39-111">O script em páginas HTML do lado do servidor se comunica com o cliente do assistente de ordenação de impressão online no qual ele está hospedado.</span><span class="sxs-lookup"><span data-stu-id="eeb39-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="eeb39-112">Essa comunicação é realizada por meio de métodos e propriedades acessados pelo objeto **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="eeb39-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="eeb39-113">Os tópicos a seguir são abordados neste documento.</span><span class="sxs-lookup"><span data-stu-id="eeb39-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="eeb39-114">Métodos e propriedades</span><span class="sxs-lookup"><span data-stu-id="eeb39-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="eeb39-115">Considerações de criação</span><span class="sxs-lookup"><span data-stu-id="eeb39-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="eeb39-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eeb39-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="eeb39-117">Métodos e propriedades</span><span class="sxs-lookup"><span data-stu-id="eeb39-117">Methods and Properties</span></span>

<span data-ttu-id="eeb39-118">Os métodos e as propriedades a seguir estão disponíveis por meio do objeto **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="eeb39-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="eeb39-119">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="eeb39-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="eeb39-120">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="eeb39-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="eeb39-121">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="eeb39-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="eeb39-122">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="eeb39-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="eeb39-123">**Setheadertext**</span><span class="sxs-lookup"><span data-stu-id="eeb39-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="eeb39-124">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="eeb39-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="eeb39-125">[**Legenda**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eeb39-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="eeb39-126">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="eeb39-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="eeb39-127">O script da página do lado do servidor chama esses métodos para notificar o cliente sobre eventos durante o procedimento de publicação.</span><span class="sxs-lookup"><span data-stu-id="eeb39-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="eeb39-128">Vejamos [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) como exemplo.</span><span class="sxs-lookup"><span data-stu-id="eeb39-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="eeb39-129">Quando o assistente exibe a primeira página HTML do lado do servidor, ele faz isso com o conhecimento dos identificadores das páginas do assistente anteriores e das páginas HTML hospedadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="eeb39-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="eeb39-130">Neste ponto do nosso exemplo, o usuário, sentado nessa primeira página HTML, clica no botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="eeb39-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="eeb39-131">O assistente envia uma notificação desse evento para o servidor.</span><span class="sxs-lookup"><span data-stu-id="eeb39-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="eeb39-132">Ao receber essa mensagem, o script do lado do servidor refere-se a seu manipulador **onback** para esse evento, que, como esta é a primeira página HTML, chama o método **FinalBack** .</span><span class="sxs-lookup"><span data-stu-id="eeb39-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="eeb39-133">Isso faz com que o assistente navegue até a página de assistente exibida antes de entrar na interface do usuário do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeb39-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="eeb39-134">Para obter uma discussão completa sobre esses métodos e propriedades, consulte a documentação para os objetos [**WebWizardHost**](/windows/desktop/shell/webwizardhost) e [**NewWDEvents**](/windows/desktop/shell/newwdevents) .</span><span class="sxs-lookup"><span data-stu-id="eeb39-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="eeb39-135">Considerações de criação</span><span class="sxs-lookup"><span data-stu-id="eeb39-135">Design Considerations</span></span>

<span data-ttu-id="eeb39-136">O HTML que compõe cada página do lado do servidor é exibido normalmente no painel do assistente.</span><span class="sxs-lookup"><span data-stu-id="eeb39-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="eeb39-137">Ao criar essas páginas, tenha em mente que uma janela do assistente não pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="eeb39-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="eeb39-138">As páginas devem, portanto, ser construídas e dimensionadas para que as barras de rolagem sejam evitadas sempre que possível para fornecer ao usuário navegação suave por meio do assistente.</span><span class="sxs-lookup"><span data-stu-id="eeb39-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="eeb39-139">Cada página HTML também deve fornecer um manipulador para eventos **OnDelete**, **OnNext** e **OnCancel** .</span><span class="sxs-lookup"><span data-stu-id="eeb39-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="eeb39-140">O manipulador **OnNext** também manipulará o evento **Finish** .</span><span class="sxs-lookup"><span data-stu-id="eeb39-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="eeb39-141">Uma página que não implementa uma função **onback** é considerada inválida e fará com que uma página de erro seja exibida.</span><span class="sxs-lookup"><span data-stu-id="eeb39-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeb39-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eeb39-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb39-143">**WebWizardHost**</span><span class="sxs-lookup"><span data-stu-id="eeb39-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="eeb39-144">**NewWDEvents**</span><span class="sxs-lookup"><span data-stu-id="eeb39-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="eeb39-145">Design do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="eeb39-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 