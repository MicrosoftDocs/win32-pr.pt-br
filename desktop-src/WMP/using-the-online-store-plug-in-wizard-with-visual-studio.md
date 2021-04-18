---
title: Usando o assistente de plug-in da loja online com o Visual Studio
description: Usando o assistente de plug-in da loja online com o Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Repositórios online do Windows Media Player, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 1 lojas online, assistente de plug-in
- Lojas online do Windows Media Player, Visual Studio
- lojas online, Visual Studio
- Digite 1 lojas online, Visual Studio
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, Visual Studio
- plug-ins, assistente de plug-in
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, Visual Studio
- Plug-ins do Windows Media Player, assistente de plug-in
- Visual Studio, assistente de lojas online do Windows Media Player
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807824"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="8b5c0-124">Usando o assistente de plug-in da loja online com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8b5c0-124">Using the Online Store Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="8b5c0-125">Depois de instalar os componentes necessários, você poderá criar rapidamente um plug-in que servirá como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-125">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="8b5c0-126">As etapas a seguir irão guiá-lo:</span><span class="sxs-lookup"><span data-stu-id="8b5c0-126">The following steps will guide you:</span></span>

1.  <span data-ttu-id="8b5c0-127">Inicie o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-127">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="8b5c0-128">No menu **arquivo** , aponte para **novo** e clique em **projeto**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-128">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="8b5c0-129">Em **tipos de projeto**, clique em **Visual C++ projetos**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-129">In **Project Types**, click **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="8b5c0-130">Em **modelos**, clique em **Assistente de lojas online do Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-130">In **Templates**, click **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="8b5c0-131">Insira um nome para seu projeto.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-131">Enter a name for your project.</span></span>
6.  <span data-ttu-id="8b5c0-132">Insira um local para seu projeto.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-132">Enter a location for your project.</span></span> <span data-ttu-id="8b5c0-133">Essa é a pasta para a qual os arquivos de projeto serão copiados.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-133">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="8b5c0-134">Clique em **OK** para iniciar o assistente.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-134">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="8b5c0-135">Selecione **tipo 1 (integração profunda)** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-135">Select **Type 1 (Deep integration)**, and click **Next**.</span></span>
9.  <span data-ttu-id="8b5c0-136">Insira um nome amigável e um distribuidor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-136">Enter a friendly name and a content distributor.</span></span> <span data-ttu-id="8b5c0-137">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-137">Click **Finish**.</span></span>
10. <span data-ttu-id="8b5c0-138">Use o ambiente de desenvolvimento do Visual Studio para compilar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-138">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="8b5c0-139">No Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute o Visual Studio com um token de acesso de administrador completo.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-139">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="8b5c0-140">Clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-140">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="8b5c0-141">Antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas include e lib em que você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-141">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="8b5c0-142">O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-142">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="8b5c0-143">Se você executou o utilitário de registro do Visual Studio que acompanha o SDK do Windows, o ambiente de desenvolvimento provavelmente já foi configurado para apontar para o SDK do Windows pastas include e lib.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-143">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="8b5c0-144">Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-144">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="8b5c0-145">Para configurar manualmente o Visual Studio, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-145">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="8b5c0-146">No menu **ferramentas** , clique em opções.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-146">On the **Tools** menu, click Options.</span></span>
2.  <span data-ttu-id="8b5c0-147">Clique em **projetos e soluções** e, em seguida, clique em **diretórios do vc + +**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-147">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="8b5c0-148">Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-148">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="8b5c0-149">Adicione os diretórios para os arquivos necessários.</span><span class="sxs-lookup"><span data-stu-id="8b5c0-149">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b5c0-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b5c0-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b5c0-151">Criando o plug-in para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="8b5c0-151">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




