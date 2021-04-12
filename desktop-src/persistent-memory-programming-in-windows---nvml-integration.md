---
description: A tecnologia de memória persistente (PM) fornece acesso em nível de byte para mídia não volátil e também reduz a latência de armazenamento ou recuperação de dados significativamente.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programação de memória persistente na integração do Windows-NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171599"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="13d91-103">Programação de memória persistente na integração do Windows-NVML</span><span class="sxs-lookup"><span data-stu-id="13d91-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="13d91-104">A tecnologia de memória persistente (PM) fornece acesso em nível de byte para mídia não volátil e também reduz a latência de armazenamento ou recuperação de dados significativamente.</span><span class="sxs-lookup"><span data-stu-id="13d91-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="13d91-105">Ele cria uma nova camada entre a memória de um sistema e o armazenamento tradicional.</span><span class="sxs-lookup"><span data-stu-id="13d91-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="13d91-106">Qualquer programa dependente ou dimensionado com gravações rápidas para um meio persistente pode se beneficiar do PM.</span><span class="sxs-lookup"><span data-stu-id="13d91-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="13d91-107">A finalidade deste artigo é descrever como a biblioteca de memória não volátil (NVML) pode ser integrada a um projeto do Visual Studio para facilitar o uso.</span><span class="sxs-lookup"><span data-stu-id="13d91-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="13d91-108">A memória persistente às vezes é também chamada de SCM (memória de classe de armazenamento).</span><span class="sxs-lookup"><span data-stu-id="13d91-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="13d91-109">PM e NVML</span><span class="sxs-lookup"><span data-stu-id="13d91-109">PM and NVML</span></span>

<span data-ttu-id="13d91-110">O primeiro suporte para memória persistente foi introduzido no Windows Server 2016 e na atualização de aniversário do Windows 10 (1607).</span><span class="sxs-lookup"><span data-stu-id="13d91-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="13d91-111">Para obter uma visão geral rápida, confira estes dois vídeos do channel9:</span><span class="sxs-lookup"><span data-stu-id="13d91-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   [<span data-ttu-id="13d91-112">Usando memória não volátil (NVDIMM-N) como armazenamento em bloco no Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="13d91-112">Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P466)
-   [<span data-ttu-id="13d91-113">Usando memória não volátil (NVDIMM-N) como armazenamento Byte-Addressable no Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="13d91-113">Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P470)

<span data-ttu-id="13d91-114">Para ajudar os desenvolvedores a aproveitar os benefícios das ofertas de memória persistente, a Microsoft também contribuiu com os esforços de trazer a biblioteca de memória não volátil (NVML) para o Windows.</span><span class="sxs-lookup"><span data-stu-id="13d91-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="13d91-115">Essa biblioteca fornece várias ferramentas para tornar os aplicativos cientes da memória persistente.</span><span class="sxs-lookup"><span data-stu-id="13d91-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="13d91-116">Por exemplo, ele contém código que permite que você crie facilmente um repositório de chave-valor com reconhecimento de PM para buscas e armazenamentos extremamente rápidos.</span><span class="sxs-lookup"><span data-stu-id="13d91-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="13d91-117">Você pode encontrar mais informações sobre o NVML, incluindo exemplos, na [biblioteca do NVM](https://pmem.io/nvml/).</span><span class="sxs-lookup"><span data-stu-id="13d91-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="13d91-118">Integrando o NVML a um projeto do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="13d91-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="13d91-119">Baixar arquivos e cabeçalhos da biblioteca NVML</span><span class="sxs-lookup"><span data-stu-id="13d91-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="13d91-120">O NVML é mantido no GitHub.</span><span class="sxs-lookup"><span data-stu-id="13d91-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="13d91-121">Você pode compilar a origem por conta própria ou apenas baixar binários compilados diretamente aqui: [NVML versão 1,2-visualização técnica do Windows](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span><span class="sxs-lookup"><span data-stu-id="13d91-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="13d91-122">Coloque os arquivos de biblioteca e os cabeçalhos em um diretório de sua escolha, por exemplo: "C: \\ NVML \\ lib" e "C: \\ NVML \\ Inc", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="13d91-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="13d91-123">Configure seu projeto da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="13d91-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="13d91-124">Abra seu projeto do Visual Studio e, no "Gerenciador de Soluções", clique com o botão direito do mouse no nome do seu projeto.</span><span class="sxs-lookup"><span data-stu-id="13d91-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="13d91-125">Abra o painel de configuração do projeto na parte inferior do pop-up resultante.</span><span class="sxs-lookup"><span data-stu-id="13d91-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="13d91-126">Navegue até "Propriedades de configuração-> C/C++" e adicione a pasta na qual você armazenou o cabeçalho (C: \\ NVML \\ Inc) no campo "diretórios de inclusão adicionais".</span><span class="sxs-lookup"><span data-stu-id="13d91-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="13d91-127">Em seguida, navegue até "Propriedades de configuração – vinculador >" e adicione a pasta na qual você armazenou a biblioteca (C: \\ NVML \\ lib) no campo "diretórios de biblioteca adicionais"</span><span class="sxs-lookup"><span data-stu-id="13d91-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="13d91-128">Em seguida, certifique-se de ter como destino o projeto para a atualização de aniversário do Windows Server 2016 ou do Windows 10:</span><span class="sxs-lookup"><span data-stu-id="13d91-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="13d91-129">Navegue até "Propriedades de configuração-> geral" e defina o campo "versão da plataforma de destino" como "10.0.14393.0" e</span><span class="sxs-lookup"><span data-stu-id="13d91-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="13d91-130">Navegue até "Propriedades de configuração-> C/C++" e adicione "NTDDI \_ version = NTDDI \_ WIN10 \_ RS1;" ao campo "pré-processador".</span><span class="sxs-lookup"><span data-stu-id="13d91-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="13d91-131">Incluir os cabeçalhos em seu código e vincular às bibliotecas necessárias</span><span class="sxs-lookup"><span data-stu-id="13d91-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="13d91-132">Neste ponto, você pode simplesmente incluir os arquivos de cabeçalho que você está procurando usar em seu código como qualquer outro arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="13d91-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="13d91-133">Por exemplo, para usar libpmem:</span><span class="sxs-lookup"><span data-stu-id="13d91-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="13d91-134">Adicione " \# include <libpmem. h>" e</span><span class="sxs-lookup"><span data-stu-id="13d91-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="13d91-135">Adicione "libpmem. lib" a "Propriedades de configuração-> linker-> Input-> dependências adicionais"</span><span class="sxs-lookup"><span data-stu-id="13d91-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="13d91-136">Neste ponto, você está pronto para chamar as funções da biblioteca diretamente no seu código e tirar proveito delas.</span><span class="sxs-lookup"><span data-stu-id="13d91-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



