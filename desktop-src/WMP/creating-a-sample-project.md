---
title: Criando um projeto de exemplo
description: Criando um projeto de exemplo
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Lojas online do Windows Media Player, criando projetos de exemplo
- lojas online, criando projetos de exemplo
- Digite 2 lojas online, criando projetos de exemplo
- Lojas online do Windows Media Player, projetos de exemplo
- lojas online, projetos de exemplo
- Digite 2 lojas online, projetos de exemplo
- Lojas online do Windows Media Player, assistente de projeto
- lojas online, assistente de projeto
- tipo 2 lojas online, assistente de projeto
- plug-ins, assistente de projeto
- Plug-ins do Windows Media Player, assistente de projeto
- Criando projetos de exemplo
- exemplos, tipo 2 lojas online
- Assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104084386"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="3750d-117">Criando um projeto de exemplo</span><span class="sxs-lookup"><span data-stu-id="3750d-117">Creating a Sample Project</span></span>

<span data-ttu-id="3750d-118">Para criar um novo projeto usando o assistente de projeto, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="3750d-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="3750d-119">Abra o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3750d-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="3750d-120">No menu **Arquivo**, aponte para **Novo** e clique em **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="3750d-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="3750d-121">Na caixa de listagem **tipos de projeto** , escolha **projetos de Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="3750d-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="3750d-122">Na caixa de listagem **modelos** , escolha **Assistente de lojas online do Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="3750d-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="3750d-123">Digite um nome e um local para o seu projeto.</span><span class="sxs-lookup"><span data-stu-id="3750d-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="3750d-124">Clique em **OK** para iniciar o assistente de projeto.</span><span class="sxs-lookup"><span data-stu-id="3750d-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="3750d-125">Selecione **tipo 2 (integração básica)** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3750d-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="3750d-126">Digite o nome amigável e a ID do distribuidor de conteúdo para seu serviço.</span><span class="sxs-lookup"><span data-stu-id="3750d-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="3750d-127">Digite a URL da página da Web que remove o serviço do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="3750d-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="3750d-128">O valor que você fornece para a ID do distribuidor de conteúdo não deve conter espaços.</span><span class="sxs-lookup"><span data-stu-id="3750d-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="3750d-129">O assistente remove todos os espaços da cadeia de caracteres que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="3750d-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="3750d-130">Clique em **Concluir** para criar o projeto.</span><span class="sxs-lookup"><span data-stu-id="3750d-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="3750d-131">O assistente gera automaticamente um novo projeto C++ que cria um plug-in de loja online tipo 2 que implementa as interfaces **IWMPSubscriptionService** e **IWMPSubscriptionService2** .</span><span class="sxs-lookup"><span data-stu-id="3750d-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="3750d-132">Cada vez que você executa o assistente, ele cria o mesmo projeto, mas o componente que é criado quando você compila o projeto tem uma ID de classe exclusiva.</span><span class="sxs-lookup"><span data-stu-id="3750d-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="3750d-133">O nome do projeto, o nome amigável e a ID do distribuidor de conteúdo também podem ser diferentes dependendo dos valores que você forneceu quando executou o assistente.</span><span class="sxs-lookup"><span data-stu-id="3750d-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="3750d-134">O projeto de exemplo registra o componente usando um nome de chave que corresponde ao valor fornecido para o nome amigável.</span><span class="sxs-lookup"><span data-stu-id="3750d-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="3750d-135">O exemplo usa o código Active Template Library (ATL) para fornecer implementações COM.</span><span class="sxs-lookup"><span data-stu-id="3750d-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="3750d-136">O assistente cria os seguintes arquivos para você:</span><span class="sxs-lookup"><span data-stu-id="3750d-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="3750d-137">*ProjectName* dll. cpp.</span><span class="sxs-lookup"><span data-stu-id="3750d-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="3750d-138">Implementa as exportações da biblioteca de vínculo dinâmico (DLL), como a função principal do ponto de entrada da DLL.</span><span class="sxs-lookup"><span data-stu-id="3750d-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="3750d-139">Também contém o mapa do objeto ATL e a declaração do módulo.</span><span class="sxs-lookup"><span data-stu-id="3750d-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="3750d-140">*ProjectName*. cpp.</span><span class="sxs-lookup"><span data-stu-id="3750d-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="3750d-141">Contém implementações padrão para os métodos das interfaces IWMPSubscriptionService e IWMPSubscriptionService2.</span><span class="sxs-lookup"><span data-stu-id="3750d-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="3750d-142">Também contém o código para definir as caixas de diálogo que o exemplo abre quando os métodos são chamados pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3750d-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="3750d-143">*ProjectName*. def. Declara as exportações de DLL.</span><span class="sxs-lookup"><span data-stu-id="3750d-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="3750d-144">StdAfx. cpp.</span><span class="sxs-lookup"><span data-stu-id="3750d-144">StdAfx.cpp.</span></span> <span data-ttu-id="3750d-145">Inclui cabeçalhos padrão.</span><span class="sxs-lookup"><span data-stu-id="3750d-145">Includes standard headers.</span></span>
-   <span data-ttu-id="3750d-146">WMP. h.</span><span class="sxs-lookup"><span data-stu-id="3750d-146">wmp.h.</span></span> <span data-ttu-id="3750d-147">O arquivo de cabeçalho do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3750d-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="3750d-148">wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="3750d-148">wmpplug.h.</span></span> <span data-ttu-id="3750d-149">O arquivo de cabeçalho de plug-in do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3750d-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="3750d-150">subscriptionservices. h.</span><span class="sxs-lookup"><span data-stu-id="3750d-150">subscriptionservices.h.</span></span> <span data-ttu-id="3750d-151">O arquivo de cabeçalho do Windows Media Player online armazena.</span><span class="sxs-lookup"><span data-stu-id="3750d-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="3750d-152">Resource. h.</span><span class="sxs-lookup"><span data-stu-id="3750d-152">resource.h.</span></span> <span data-ttu-id="3750d-153">Contém definições de recurso.</span><span class="sxs-lookup"><span data-stu-id="3750d-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="3750d-154">**ProjectName**. h.</span><span class="sxs-lookup"><span data-stu-id="3750d-154">**ProjectName**.h.</span></span> <span data-ttu-id="3750d-155">Contém definições de classe para o objeto de loja online e as caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3750d-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="3750d-156">Define a ID de classe do objeto e a constante de ID do distribuidor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3750d-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="3750d-157">StdAfx. h.</span><span class="sxs-lookup"><span data-stu-id="3750d-157">StdAfx.h.</span></span> <span data-ttu-id="3750d-158">Contém inclusões de sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="3750d-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="3750d-159">*ProjectName*. rc.</span><span class="sxs-lookup"><span data-stu-id="3750d-159">*ProjectName*.rc.</span></span> <span data-ttu-id="3750d-160">O arquivo de script do recurso.</span><span class="sxs-lookup"><span data-stu-id="3750d-160">The resource script file.</span></span> <span data-ttu-id="3750d-161">Ele contém definições para os recursos e controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3750d-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="3750d-162">Isso também é onde a tabela de cadeia de caracteres é armazenada.</span><span class="sxs-lookup"><span data-stu-id="3750d-162">This is also where the string table is stored.</span></span> <span data-ttu-id="3750d-163">A tabela de cadeia de caracteres contém o nome do projeto e constantes de cadeia de caracteres de nome amigável.</span><span class="sxs-lookup"><span data-stu-id="3750d-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="3750d-164">Normalmente, você trabalha com esse arquivo no editor de recursos do Visual Studio, não como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="3750d-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="3750d-165">*ProjectName*. rgs.</span><span class="sxs-lookup"><span data-stu-id="3750d-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="3750d-166">O arquivo de script do registro.</span><span class="sxs-lookup"><span data-stu-id="3750d-166">The registry script file.</span></span> <span data-ttu-id="3750d-167">Esse arquivo contém as informações usadas para adicionar a classe de componente ao registro para que o Windows Media Player possa localizá-la.</span><span class="sxs-lookup"><span data-stu-id="3750d-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="3750d-168">Você pode alterar o nome da chave para o serviço neste arquivo.</span><span class="sxs-lookup"><span data-stu-id="3750d-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="3750d-169">Você deve definir o endereço base para sua DLL como 0x0F100000 para evitar conflitos com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3750d-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3750d-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3750d-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3750d-171">**Criando o plug-in para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="3750d-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="3750d-172">**Interface IWMPSubscriptionService**</span><span class="sxs-lookup"><span data-stu-id="3750d-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="3750d-173">**Interface IWMPSubscriptionService2**</span><span class="sxs-lookup"><span data-stu-id="3750d-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




