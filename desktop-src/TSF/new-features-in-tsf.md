---
title: Novos recursos no TSF
description: Com o lançamento do Microsoft WindowsXP Service Pack1, a TSF (estrutura de serviços de texto) tem vários recursos novos.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- TSF (estrutura de serviços de texto), novos recursos
- TSF (estrutura de serviços de texto), novos recursos
- serviços de texto, novos recursos
- Aplicativos habilitados para TSF, novos recursos
- TSF (estrutura de serviços de texto), suporte avançado
- TSF (estrutura de serviços de texto), suporte avançado
- serviços de texto, suporte avançado
- Aplicativos habilitados para TSF, suporte avançado
- TSF (estrutura de serviços de texto), edição avançada
- TSF (estrutura de serviços de texto), edição avançada
- serviços de texto, edição avançada
- Aplicativos habilitados para TSF, edição avançada
- Edição avançada
- TSF (estrutura de serviços de texto), segurança
- TSF (estrutura de serviços de texto), segurança
- serviços de texto, segurança
- Aplicativos habilitados para TSF, segurança
- segurança para TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366106"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="1b47a-121">Novos recursos no TSF</span><span class="sxs-lookup"><span data-stu-id="1b47a-121">New Features in TSF</span></span>

<span data-ttu-id="1b47a-122">Com o lançamento do Microsoft WindowsXP Service Pack1, a TSF (estrutura de serviços de texto) tem vários recursos novos.</span><span class="sxs-lookup"><span data-stu-id="1b47a-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="1b47a-123">Suporte estendido de serviços de texto avançados</span><span class="sxs-lookup"><span data-stu-id="1b47a-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="1b47a-124">O suporte foi adicionado ao TSF e ao Windows para fornecer uma interface de usuário consistente para todos os aplicativos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b47a-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="1b47a-125">Esse novo suporte permite que os aplicativos herdados ou controles que não reconheçam o TSF aproveitem alguns serviços de texto avançados gratuitamente.</span><span class="sxs-lookup"><span data-stu-id="1b47a-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="1b47a-126">Por exemplo, o ditado de fala e o manuscrito agora podem ser usados para inserir texto em um documento em qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b47a-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="1b47a-127">Esse novo recurso está disponível apenas para o WindowsXP Service Pack1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1b47a-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="1b47a-128">Ela é desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="1b47a-128">It is turned off by default.</span></span> <span data-ttu-id="1b47a-129">Para habilitá-lo, clique na caixa de seleção na nova guia **avançado** na parte de **serviços de texto e idiomas de entrada** do painel de controle **Opções regionais e de idiomas** .</span><span class="sxs-lookup"><span data-stu-id="1b47a-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![suporte a aplicativos sem reconhecimento no painel de controle do TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="1b47a-131">Suporte para edição avançada</span><span class="sxs-lookup"><span data-stu-id="1b47a-131">Rich Edit Support</span></span>

<span data-ttu-id="1b47a-132">[Edição avançada do Microsoft®](../controls/rich-edit-controls.md) A versão 4,1, usada por aplicativos para exibir e editar texto com caracteres especiais e formatação de parágrafo, agora expõe a funcionalidade TSF.</span><span class="sxs-lookup"><span data-stu-id="1b47a-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="1b47a-133">Por padrão, esse suporte é desativado.</span><span class="sxs-lookup"><span data-stu-id="1b47a-133">By default this support is turned off.</span></span> <span data-ttu-id="1b47a-134">Para habilitar o TSF no Rich Edit, um aplicativo de hospedagem envia uma mensagem de janela especial para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="1b47a-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="1b47a-135">Aprimoramentos de segurança</span><span class="sxs-lookup"><span data-stu-id="1b47a-135">Security Improvements</span></span>

<span data-ttu-id="1b47a-136">A segurança e a robustez do TSF foram substancialmente aperfeiçoadas, para reduzir a probabilidade de um programa hostil ser capaz de acessar a pilha, heap ou outros locais de memória segura.</span><span class="sxs-lookup"><span data-stu-id="1b47a-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="1b47a-137">A segurança dos aplicativos de exemplo do SDK (Software Development Kit) e dos serviços de texto também foi aprimorada.</span><span class="sxs-lookup"><span data-stu-id="1b47a-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 