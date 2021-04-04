---
title: Introdução com o assistente de plug-in
description: Introdução com o assistente de plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Plug-ins do Windows Media Player, instalando o assistente de plug-in
- plug-ins, instalando o assistente de plug-in
- Criando plug-ins, instalando o assistente de plug-in
- Assistente de plug-in do Windows Media Player, instalando
- Instalando o assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916480"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="02eb1-109">Introdução com o assistente de plug-in</span><span class="sxs-lookup"><span data-stu-id="02eb1-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="02eb1-110">Para configurar seu ambiente de desenvolvimento para a criação de plug-ins do Windows Media Player, você deve instalar os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="02eb1-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="02eb1-111">Microsoft Visual Studio .NET 2003 ou posterior</span><span class="sxs-lookup"><span data-stu-id="02eb1-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="02eb1-112">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="02eb1-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="02eb1-113">SDK do Windows, que inclui o SDK do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="02eb1-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="02eb1-114">Assistente de plug-in do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="02eb1-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="02eb1-115">Instalando o assistente</span><span class="sxs-lookup"><span data-stu-id="02eb1-115">Installing the Wizard</span></span>

<span data-ttu-id="02eb1-116">Execute as etapas a seguir para instalar o assistente de plug-in do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02eb1-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="02eb1-117">Localize a pasta onde você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="02eb1-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="02eb1-118">Expanda a pasta para exibir suas subpastas e navegue até exemplos \\ \\ assistentes de WMP multimídia \\ \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="02eb1-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="02eb1-119">Localize os três arquivos a seguir:</span><span class="sxs-lookup"><span data-stu-id="02eb1-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="02eb1-120">wmpwiz. vsz</span><span class="sxs-lookup"><span data-stu-id="02eb1-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="02eb1-121">wmpwiz. vsdir</span><span class="sxs-lookup"><span data-stu-id="02eb1-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="02eb1-122">wmpwiz. ico</span><span class="sxs-lookup"><span data-stu-id="02eb1-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="02eb1-123">Usando um editor de texto, como o bloco de notas, edite o arquivo wmpwiz. vsz.</span><span class="sxs-lookup"><span data-stu-id="02eb1-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="02eb1-124">Localize a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="02eb1-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="02eb1-125">Altere `<VsWizardEngine version goes here>` para um dos valores a seguir, dependendo da versão do Visual Studio instalada.</span><span class="sxs-lookup"><span data-stu-id="02eb1-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="02eb1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="02eb1-126">Value</span></span>              | <span data-ttu-id="02eb1-127">Versão do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02eb1-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="02eb1-128">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="02eb1-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="02eb1-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="02eb1-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="02eb1-130">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="02eb1-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="02eb1-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="02eb1-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="02eb1-132">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="02eb1-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="02eb1-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="02eb1-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="02eb1-134">Localize a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="02eb1-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="02eb1-135">Altere `<path to wmpwiz directory goes here>` para o caminho onde os arquivos do assistente estão localizados.</span><span class="sxs-lookup"><span data-stu-id="02eb1-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="02eb1-136">Por exemplo, suponha que você tenha o Visual Studio 2008 e que os arquivos do assistente estejam aqui: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WMP \\ assistentes \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="02eb1-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="02eb1-137">Em seguida, o arquivo wmpwiz. vsz teria esta aparência:</span><span class="sxs-lookup"><span data-stu-id="02eb1-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="02eb1-138">Localize a pasta onde você instalou o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="02eb1-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="02eb1-139">Expanda a pasta para exibir suas subpastas e localize uma pasta chamada vcprojects.</span><span class="sxs-lookup"><span data-stu-id="02eb1-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="02eb1-140">Copie os três arquivos listados na etapa 2 para a pasta vcprojects.</span><span class="sxs-lookup"><span data-stu-id="02eb1-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="02eb1-141">O assistente agora está instalado.</span><span class="sxs-lookup"><span data-stu-id="02eb1-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02eb1-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02eb1-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02eb1-143">Criando um plug-in</span><span class="sxs-lookup"><span data-stu-id="02eb1-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="02eb1-144">Usando o assistente de plug-in com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02eb1-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




