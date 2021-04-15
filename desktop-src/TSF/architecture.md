---
title: Arquitetura (estrutura de serviços de texto)
description: Arquitetura
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- TSF (estrutura de serviços de texto), arquitetura
- TSF (estrutura de serviços de texto), arquitetura
- serviços de texto, arquitetura
- Aplicativos habilitados para TSF, arquitetura
- TSF (estrutura de serviços de texto), componentes
- TSF (estrutura de serviços de texto), componentes
- serviços de texto, componentes
- Aplicativos habilitados para TSF, componentes
- TSF (estrutura de serviços de texto), aplicativos
- TSF (estrutura de serviços de texto), aplicativos
- serviços de texto, aplicativos
- Aplicativos habilitados para TSF, sobre
- TSF (estrutura de serviços de texto), serviços de texto
- TSF (estrutura de serviços de texto), serviços de texto
- serviços de texto, sobre
- Aplicativos habilitados para TSF, serviços de texto
- TSF (estrutura de serviços de texto), Gerenciador de TSF
- TSF (estrutura de serviços de texto), Gerenciador de TSF
- serviços de texto, Gerenciador de TSF
- Aplicativos habilitados para TSF, Gerenciador de TSF
- Gerenciador de TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104569707"
---
# <a name="architecture-text-services-framework"></a><span data-ttu-id="c5c86-124">Arquitetura (estrutura de serviços de texto)</span><span class="sxs-lookup"><span data-stu-id="c5c86-124">Architecture (Text Services Framework)</span></span>

<span data-ttu-id="c5c86-125">A estrutura de serviços de texto inclui três componentes principais:</span><span class="sxs-lookup"><span data-stu-id="c5c86-125">Text Services Framework includes three primary components:</span></span>

-   <span data-ttu-id="c5c86-126">**Aplicativos:** As operações de aplicativo normalmente incluem exibição, edição direta e armazenamento de texto.</span><span class="sxs-lookup"><span data-stu-id="c5c86-126">**Applications:** Application operations typically include display, direct editing, and storage of text.</span></span> <span data-ttu-id="c5c86-127">Um aplicativo fornece acesso ao texto implementando um servidor COM que dá suporte a determinadas interfaces e se comunica com o TSF usando interfaces que o Gerenciador TSF expõe.</span><span class="sxs-lookup"><span data-stu-id="c5c86-127">An application provides access to text by implementing a COM server that supports certain interfaces and communicates with TSF using interfaces that the TSF manager exposes.</span></span> <span data-ttu-id="c5c86-128">Em toda esta documentação, o termo, aplicativo, se refere a um aplicativo habilitado para TSF, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c5c86-128">Throughout this documentation, the term, application, refers to a TSF-enabled application, unless otherwise specified.</span></span>
-   <span data-ttu-id="c5c86-129">**Serviços de texto:** Um serviço de texto funciona como um provedor de texto para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5c86-129">**Text Services:** A text service functions as a text provider to an application.</span></span> <span data-ttu-id="c5c86-130">Um serviço de texto pode obter texto de e gravar texto em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5c86-130">A text service can obtain text from, and write text to, an application.</span></span> <span data-ttu-id="c5c86-131">Um serviço de texto também pode associar dados e propriedades com um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="c5c86-131">A text service can also associate data and properties with a block of text.</span></span> <span data-ttu-id="c5c86-132">Um serviço de texto é implementado como um servidor em processo COM que se registra no TSF.</span><span class="sxs-lookup"><span data-stu-id="c5c86-132">A text service is implemented as a COM in-proc server that registers itself with TSF.</span></span> <span data-ttu-id="c5c86-133">Quando registrado, o usuário interage com o serviço de texto usando a barra de idiomas ou os atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="c5c86-133">When registered, the user interacts with the text service using the language bar or keyboard shortcuts.</span></span> <span data-ttu-id="c5c86-134">Vários serviços de texto podem ser instalados.</span><span class="sxs-lookup"><span data-stu-id="c5c86-134">Multiple text services can be installed.</span></span>
-   <span data-ttu-id="c5c86-135">**Gerenciador de TSF:** O Gerenciador de TSF funciona como um mediador entre um aplicativo e um ou mais serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="c5c86-135">**TSF Manager:** The TSF manager functions as a mediator between an application and one or more text services.</span></span> <span data-ttu-id="c5c86-136">Um serviço de texto nunca interage diretamente com um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5c86-136">A text service never interacts directly with an application.</span></span> <span data-ttu-id="c5c86-137">Toda a comunicação passa pelo Gerenciador de TSF.</span><span class="sxs-lookup"><span data-stu-id="c5c86-137">All communication passes through the TSF manager.</span></span> <span data-ttu-id="c5c86-138">O Gerenciador de TSF é implementado pelo sistema operacional e não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="c5c86-138">The TSF manager is implemented by the operating system and cannot be replaced.</span></span> <span data-ttu-id="c5c86-139">Ao longo desta documentação, o termo, gerente, refere-se ao Gerenciador do TSF, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c5c86-139">Throughout this documentation, the term, manager, refers to the TSF manager, unless otherwise specified.</span></span>

<span data-ttu-id="c5c86-140">A ilustração a seguir mostra os principais elementos de arquitetura do TSF.</span><span class="sxs-lookup"><span data-stu-id="c5c86-140">The following illustration shows the primary architectural elements of TSF.</span></span>

![arquitetura da estrutura de serviços de texto](images/tsf-arch.gif)

<span data-ttu-id="c5c86-142">Com essa arquitetura, o Gerenciador do TSF fornece uma camada de abstração entre aplicativos e serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="c5c86-142">With this architecture, the TSF manager provides an abstraction layer between applications and text services.</span></span> <span data-ttu-id="c5c86-143">Essa camada de abstração permite que um aplicativo e um ou mais serviços de texto compartilhem texto e permite que o Gerenciador do TSF gerencie serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="c5c86-143">This abstraction layer enables an application and one or more text services to share text, and it enables the TSF manager to manage text services.</span></span>

 

 




