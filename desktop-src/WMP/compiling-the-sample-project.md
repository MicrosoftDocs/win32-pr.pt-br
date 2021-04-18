---
title: Compilando o projeto de exemplo
description: Compilando o projeto de exemplo
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Lojas online do Windows Media Player, compilando projetos de exemplo
- lojas online, compilando projetos de exemplo
- Digite 2 lojas online, compilando projetos de exemplo
- Lojas online do Windows Media Player, projetos de exemplo
- lojas online, projetos de exemplo
- Digite 2 lojas online, projetos de exemplo
- Lojas online do Windows Media Player, assistente de projeto
- lojas online, assistente de projeto
- tipo 2 lojas online, assistente de projeto
- plug-ins, assistente de projeto
- Plug-ins do Windows Media Player, assistente de projeto
- compilando projetos de exemplo
- exemplos, tipo 2 lojas online
- Assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770514"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="b7a8f-117">Compilando o projeto de exemplo</span><span class="sxs-lookup"><span data-stu-id="b7a8f-117">Compiling the Sample Project</span></span>

<span data-ttu-id="b7a8f-118">O assistente gera todos os arquivos necessários para compilar o projeto de exemplo, para que você não precise alterar as configurações de projeto padrão.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="b7a8f-119">No Visual Studio, no menu **Compilar** , clique em **Compilar solução** para compilar e registrar o componente com.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="b7a8f-120">Por padrão, a configuração de depuração está ativa.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="b7a8f-121">No Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute o Visual Studio com um token de acesso de administrador completo.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="b7a8f-122">Clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="b7a8f-123">Antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas include e lib em que você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="b7a8f-124">O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="b7a8f-125">Se você executou o utilitário de registro do Visual Studio que acompanha o SDK do Windows Vista, seu ambiente de desenvolvimento provavelmente já foi configurado para apontar para as pastas de SDK do Windows incluir e lib.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="b7a8f-126">Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="b7a8f-127">Para configurar manualmente o Visual Studio, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="b7a8f-128">No menu **Ferramentas** , clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="b7a8f-129">Clique em **projetos e soluções** e, em seguida, clique em **diretórios do vc + +**.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="b7a8f-130">Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="b7a8f-131">Adicione os diretórios para os arquivos necessários.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7a8f-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7a8f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7a8f-133">Criando o plug-in para uma loja online tipo 2</span><span class="sxs-lookup"><span data-stu-id="b7a8f-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




