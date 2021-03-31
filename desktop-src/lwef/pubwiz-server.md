---
title: Design de Server-Side
description: As funções do lado do servidor se comunicam com o assistente do cliente por meio do objeto Windows. external. O script do lado do servidor fornece essas funções para responder a eventos do assistente e para recuperar informações sobre o assistente.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- assistentes de publicação, design do lado do servidor
- janela. external, assistentes de publicação
- assistentes de publicação, janela. externa
- assistentes de publicação, funções de script de navegação
- scripts, assistentes de publicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917310"
---
# <a name="server-side-design"></a><span data-ttu-id="32bb9-109">Design de Server-Side</span><span class="sxs-lookup"><span data-stu-id="32bb9-109">Server-Side Design</span></span>

<span data-ttu-id="32bb9-110">As funções do lado do servidor se comunicam com o assistente do cliente por meio do objeto **Windows. external** .</span><span class="sxs-lookup"><span data-stu-id="32bb9-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="32bb9-111">O script do lado do servidor fornece essas funções para responder a eventos do assistente e para recuperar informações sobre o assistente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="32bb9-112">Os tópicos a seguir são abordados neste documento.</span><span class="sxs-lookup"><span data-stu-id="32bb9-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="32bb9-113">Implementando funções de script de navegação</span><span class="sxs-lookup"><span data-stu-id="32bb9-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="32bb9-114">Voltar ()</span><span class="sxs-lookup"><span data-stu-id="32bb9-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="32bb9-115">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="32bb9-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="32bb9-116">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="32bb9-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="32bb9-117">Outros métodos e propriedades</span><span class="sxs-lookup"><span data-stu-id="32bb9-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="32bb9-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="32bb9-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="32bb9-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32bb9-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="32bb9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32bb9-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="32bb9-121">Implementando funções de script de navegação</span><span class="sxs-lookup"><span data-stu-id="32bb9-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="32bb9-122">O script do lado do servidor em cada página HTML responde aos botões de navegação por meio de funções para **onvoltar**, **OnNext** e **OnCancel**.</span><span class="sxs-lookup"><span data-stu-id="32bb9-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="32bb9-123">Essas funções devem ser acessíveis por meio de **IHTMLDocument:: get \_ script** no cliente e não têm parâmetros.</span><span class="sxs-lookup"><span data-stu-id="32bb9-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="32bb9-124">Voltar ()</span><span class="sxs-lookup"><span data-stu-id="32bb9-124">OnBack()</span></span>

-   <span data-ttu-id="32bb9-125">Responde quando o usuário clica no botão de **volta** no assistente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="32bb9-126">Se a página atual do servidor for a primeira página do lado do servidor, chame **Window. external. FinalBack** para instruir o cliente a navegar até a página anterior do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="32bb9-127">Se a página atual do servidor não for a primeira página do lado do servidor, navegue até a página anterior do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="32bb9-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="32bb9-128">Essa função deve ser implementada para cada página.</span><span class="sxs-lookup"><span data-stu-id="32bb9-128">This function must be implemented for each page.</span></span> <span data-ttu-id="32bb9-129">Qualquer página que não faça isso é considerada inválida e exibe uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="32bb9-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="32bb9-130">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="32bb9-130">OnNext()</span></span>

-   <span data-ttu-id="32bb9-131">Responde quando o usuário clica em **Avançar** no assistente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="32bb9-132">Se a página atual do servidor for a última página do lado do servidor, chame **Window. external. FinalNext** para instruir o cliente a navegar até a próxima página do lado do cliente ou para concluir o assistente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="32bb9-133">Se a página atual do servidor não for a última página do lado do servidor, navegue até a próxima página do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="32bb9-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="32bb9-134">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="32bb9-134">OnCancel()</span></span>

-   <span data-ttu-id="32bb9-135">Responde quando o usuário clica em **Cancelar** no assistente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="32bb9-136">A interface de usuário deve ser projetada para que o usuário possa cancelar a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="32bb9-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="32bb9-137">Depois que qualquer processamento na função **OnCancel** for processado, o cliente fechará o assistente.</span><span class="sxs-lookup"><span data-stu-id="32bb9-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="32bb9-138">Outros métodos e propriedades</span><span class="sxs-lookup"><span data-stu-id="32bb9-138">Other Methods and Properties</span></span>

<span data-ttu-id="32bb9-139">As funções implementadas pelo cliente são acessadas por meio do **Windows. external**, assim como propriedades.</span><span class="sxs-lookup"><span data-stu-id="32bb9-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="32bb9-140">Os serviços disponíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="32bb9-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="32bb9-141">Métodos</span><span class="sxs-lookup"><span data-stu-id="32bb9-141">Methods</span></span>

-   [<span data-ttu-id="32bb9-142">**Setheadertext**</span><span class="sxs-lookup"><span data-stu-id="32bb9-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="32bb9-143">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="32bb9-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="32bb9-144">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="32bb9-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="32bb9-145">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32bb9-145">Properties</span></span>

-   <span data-ttu-id="32bb9-146">[**Legenda**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32bb9-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="32bb9-147">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="32bb9-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="32bb9-148">O exemplo de código a seguir mostra o código do lado do servidor para uma página de assistente simples que implementa a página de erro do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="32bb9-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="32bb9-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32bb9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32bb9-150">Design do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="32bb9-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="32bb9-151">Registrando um serviço</span><span class="sxs-lookup"><span data-stu-id="32bb9-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 