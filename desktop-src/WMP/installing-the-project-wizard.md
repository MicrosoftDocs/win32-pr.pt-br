---
title: Instalando o assistente de projeto
description: Instalando o assistente de projeto
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 2 lojas online, plug-ins
- Repositórios online do Windows Media Player, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 2 lojas online, assistente de plug-in
- Lojas online do Windows Media Player, assistente de projeto
- lojas online, assistente de projeto
- tipo 2 lojas online, assistente de projeto
- Armazenamentos online do Windows Media Player, instalando o assistente de plug-in
- lojas online, instalando o assistente de plug-in
- tipo 2 lojas online, instalando o assistente de plug-in
- Armazenamentos online do Windows Media Player, assistente de instalação de projeto
- repositórios online, assistente de instalação de projeto
- tipo 2 lojas online, assistente de instalação de projeto
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, tipo 2 lojas online
- plug-ins, instalando o assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins, assistente de instalação de projeto
- plug-ins, assistente de projeto
- Plug-ins do Windows Media Player, tipo 2 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, instalando o assistente de plug-in
- Plug-ins do Windows Media Player, assistente de plug-in
- Plug-ins do Windows Media Player, assistente para instalação de projeto
- Plug-ins do Windows Media Player, assistente de projeto
- Instalando o assistente de plug-in
- Assistente de plug-in
- Assistente de instalação de projeto
- Assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636398"
---
# <a name="installing-the-project-wizard"></a><span data-ttu-id="d266e-136">Instalando o assistente de projeto</span><span class="sxs-lookup"><span data-stu-id="d266e-136">Installing the Project Wizard</span></span>

<span data-ttu-id="d266e-137">Para configurar seu ambiente de desenvolvimento para criar plug-ins de loja online do tipo 2, você deve instalar os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="d266e-137">To set up your development environment for creating type 2 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="d266e-138">Microsoft Visual Studio .NET 2003 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d266e-138">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="d266e-139">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d266e-139">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="d266e-140">SDK do Windows, que inclui o SDK do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d266e-140">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="d266e-141">Assistente de plug-in da loja online</span><span class="sxs-lookup"><span data-stu-id="d266e-141">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="d266e-142">Instalando o assistente</span><span class="sxs-lookup"><span data-stu-id="d266e-142">Installing the Wizard</span></span>

<span data-ttu-id="d266e-143">Use as etapas a seguir para instalar o assistente de plug-in da loja online no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d266e-143">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="d266e-144">Localize a pasta onde você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d266e-144">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="d266e-145">Expanda a pasta para exibir suas subpastas e navegue até exemplos \\ \\ serviços de assistentes de WMP de multimídia \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="d266e-145">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="d266e-146">Localize os três arquivos a seguir:</span><span class="sxs-lookup"><span data-stu-id="d266e-146">Locate the following three files:</span></span>
    -   <span data-ttu-id="d266e-147">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="d266e-147">wmpservices.vsz</span></span>
    -   <span data-ttu-id="d266e-148">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="d266e-148">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="d266e-149">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="d266e-149">wmpservices.ico</span></span>
3.  <span data-ttu-id="d266e-150">Usando um editor de texto como o bloco de notas, edite o arquivo wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="d266e-150">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="d266e-151">Localize a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="d266e-151">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="d266e-152">Altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo da versão do Visual Studio instalada.</span><span class="sxs-lookup"><span data-stu-id="d266e-152">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="d266e-153">Valor</span><span class="sxs-lookup"><span data-stu-id="d266e-153">Value</span></span>              | <span data-ttu-id="d266e-154">Versão do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d266e-154">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="d266e-155">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="d266e-155">VsWizardEngine.7.1</span></span> | <span data-ttu-id="d266e-156">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="d266e-156">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="d266e-157">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="d266e-157">VsWizardEngine.8.0</span></span> | <span data-ttu-id="d266e-158">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="d266e-158">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="d266e-159">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="d266e-159">VsWizardEngine.9.0</span></span> | <span data-ttu-id="d266e-160">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="d266e-160">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="d266e-161">Localize a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="d266e-161">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="d266e-162">Altere `<path to wmpservices directory goes here>` para o caminho onde os arquivos do assistente estão localizados.</span><span class="sxs-lookup"><span data-stu-id="d266e-162">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="d266e-163">Por exemplo, suponha que você tenha o Visual Studio 2008 e que os arquivos do assistente estejam aqui: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WMP \\ assistentes \\ serviços.</span><span class="sxs-lookup"><span data-stu-id="d266e-163">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="d266e-164">Em seguida, o arquivo wmpservices. vsz teria esta aparência:</span><span class="sxs-lookup"><span data-stu-id="d266e-164">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="d266e-165">Localize a pasta onde você instalou o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d266e-165">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="d266e-166">Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.</span><span class="sxs-lookup"><span data-stu-id="d266e-166">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="d266e-167">Copie os três arquivos listados na etapa 2 para a pasta vcprojects.</span><span class="sxs-lookup"><span data-stu-id="d266e-167">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="d266e-168">O assistente agora está instalado.</span><span class="sxs-lookup"><span data-stu-id="d266e-168">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d266e-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d266e-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d266e-170">**Criando o plug-in para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d266e-170">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




