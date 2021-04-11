---
title: Usando o assistente de plug-in com o Visual Studio
description: Usando o assistente de plug-in com o Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Plug-ins do Windows Media Player, Visual Studio
- plug-ins, Visual Studio
- Criando plug-ins, Visual Studio
- Assistente de plug-in do Windows Media Player, Visual Studio
- Visual Studio, assistente de plug-in do Windows Media Player
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292367"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="a2d18-109">Usando o assistente de plug-in com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a2d18-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="a2d18-110">Depois de instalar os componentes necessários, você poderá criar rapidamente um plug-in que servirá como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="a2d18-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="a2d18-111">As etapas a seguir vão orientá-lo.</span><span class="sxs-lookup"><span data-stu-id="a2d18-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="a2d18-112">Inicie o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a2d18-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="a2d18-113">No menu **arquivo** , aponte para **novo** e clique em **projeto**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="a2d18-114">Em **tipos de projeto**, selecione **projetos de Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="a2d18-115">Em **modelos**, selecione **Assistente de plug-in do Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="a2d18-116">Insira um nome para seu projeto.</span><span class="sxs-lookup"><span data-stu-id="a2d18-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="a2d18-117">Insira um local para seu projeto.</span><span class="sxs-lookup"><span data-stu-id="a2d18-117">Enter a location for your project.</span></span> <span data-ttu-id="a2d18-118">Essa é a pasta para a qual os arquivos de projeto serão copiados.</span><span class="sxs-lookup"><span data-stu-id="a2d18-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="a2d18-119">Clique em **OK** para iniciar o assistente.</span><span class="sxs-lookup"><span data-stu-id="a2d18-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="a2d18-120">Selecione o tipo de plug-in que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="a2d18-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="a2d18-121">Conclua todas as caixas de diálogo restantes no assistente.</span><span class="sxs-lookup"><span data-stu-id="a2d18-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="a2d18-122">Use o ambiente de desenvolvimento do Visual Studio para compilar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="a2d18-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="a2d18-123">No Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute o Visual Studio com um token de acesso de administrador completo.</span><span class="sxs-lookup"><span data-stu-id="a2d18-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="a2d18-124">Clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="a2d18-125">Antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas include e lib em que você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="a2d18-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="a2d18-126">O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.</span><span class="sxs-lookup"><span data-stu-id="a2d18-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="a2d18-127">Se você executou o utilitário de registro do Visual Studio que acompanha o SDK do Windows, o ambiente de desenvolvimento provavelmente já foi configurado para apontar para o SDK do Windows pastas include e lib.</span><span class="sxs-lookup"><span data-stu-id="a2d18-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="a2d18-128">Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="a2d18-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="a2d18-129">Para configurar manualmente o Visual Studio, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="a2d18-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="a2d18-130">No menu **Ferramentas** , clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="a2d18-131">Clique em **projetos e soluções** e, em seguida, clique em **diretórios do vc + +**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="a2d18-132">Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="a2d18-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="a2d18-133">Adicione os diretórios para os arquivos necessários.</span><span class="sxs-lookup"><span data-stu-id="a2d18-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2d18-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2d18-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d18-135">Criando um plug-in</span><span class="sxs-lookup"><span data-stu-id="a2d18-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




