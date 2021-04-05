---
title: Instalando o assistente de plug-in da loja online
description: Instalando o assistente de plug-in da loja online
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Repositórios online do Windows Media Player, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 1 lojas online, assistente de plug-in
- Armazenamentos online do Windows Media Player, instalando o assistente de plug-in
- lojas online, instalando o assistente de plug-in
- Digite 1 lojas online, instalando o assistente de plug-in
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, instalando o assistente de plug-in
- plug-ins, assistente de plug-in
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, instalando o assistente de plug-in
- Plug-ins do Windows Media Player, assistente de plug-in
- Instalando o assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005633"
---
# <a name="installing-the-online-store-plug-in-wizard"></a><span data-ttu-id="90a60-124">Instalando o assistente de plug-in da loja online</span><span class="sxs-lookup"><span data-stu-id="90a60-124">Installing the Online Store Plug-in Wizard</span></span>

<span data-ttu-id="90a60-125">Para configurar seu ambiente de desenvolvimento para criar plug-ins de loja online do tipo 1, você deve instalar os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="90a60-125">To set up your development environment for creating type 1 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="90a60-126">Microsoft Visual Studio 2005 ou posterior</span><span class="sxs-lookup"><span data-stu-id="90a60-126">Microsoft Visual Studio 2005 or later</span></span>
-   <span data-ttu-id="90a60-127">Windows Media Player 11 ou posterior</span><span class="sxs-lookup"><span data-stu-id="90a60-127">Windows Media Player 11 or later</span></span>
-   <span data-ttu-id="90a60-128">SDK do Windows, que inclui o SDK do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="90a60-128">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="90a60-129">Assistente de plug-in da loja online</span><span class="sxs-lookup"><span data-stu-id="90a60-129">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="90a60-130">Instalando o assistente</span><span class="sxs-lookup"><span data-stu-id="90a60-130">Installing the Wizard</span></span>

<span data-ttu-id="90a60-131">Use as etapas a seguir para instalar o assistente de plug-in da loja online no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90a60-131">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="90a60-132">Localize a pasta onde você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="90a60-132">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="90a60-133">Expanda a pasta para exibir suas subpastas e navegue até exemplos \\ \\ serviços de assistentes de WMP de multimídia \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="90a60-133">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="90a60-134">Localize os três arquivos a seguir:</span><span class="sxs-lookup"><span data-stu-id="90a60-134">Locate the following three files:</span></span>
    -   <span data-ttu-id="90a60-135">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="90a60-135">wmpservices.vsz</span></span>
    -   <span data-ttu-id="90a60-136">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="90a60-136">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="90a60-137">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="90a60-137">wmpservices.ico</span></span>
3.  <span data-ttu-id="90a60-138">Usando um editor de texto como o bloco de notas, edite o arquivo wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="90a60-138">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="90a60-139">Localize a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="90a60-139">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="90a60-140">Altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo da versão do Visual Studio instalada.</span><span class="sxs-lookup"><span data-stu-id="90a60-140">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="90a60-141">Valor</span><span class="sxs-lookup"><span data-stu-id="90a60-141">Value</span></span>              | <span data-ttu-id="90a60-142">Versão do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90a60-142">Visual Studio version</span></span> |
    |--------------------|-----------------------|
    | <span data-ttu-id="90a60-143">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="90a60-143">VsWizardEngine.8.0</span></span> | <span data-ttu-id="90a60-144">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="90a60-144">Visual Studio 2005</span></span>    |
    | <span data-ttu-id="90a60-145">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="90a60-145">VsWizardEngine.9.0</span></span> | <span data-ttu-id="90a60-146">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="90a60-146">Visual Studio 2008</span></span>    |

    

     

    <span data-ttu-id="90a60-147">Localize a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="90a60-147">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="90a60-148">Altere `<path to wmpservices directory goes here>` para o caminho onde os arquivos do assistente estão localizados.</span><span class="sxs-lookup"><span data-stu-id="90a60-148">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="90a60-149">Por exemplo, suponha que você tenha o Visual Studio 2008 e que os arquivos do assistente estejam aqui: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WMP \\ assistentes \\ serviços.</span><span class="sxs-lookup"><span data-stu-id="90a60-149">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="90a60-150">Em seguida, o arquivo wmpservices. vsz teria esta aparência:</span><span class="sxs-lookup"><span data-stu-id="90a60-150">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="90a60-151">Localize a pasta onde você instalou o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90a60-151">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="90a60-152">Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.</span><span class="sxs-lookup"><span data-stu-id="90a60-152">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="90a60-153">Copie os três arquivos listados na etapa 2 para a pasta vcprojects.</span><span class="sxs-lookup"><span data-stu-id="90a60-153">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="90a60-154">O assistente agora está instalado.</span><span class="sxs-lookup"><span data-stu-id="90a60-154">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90a60-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90a60-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90a60-156">Criando o plug-in para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="90a60-156">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




