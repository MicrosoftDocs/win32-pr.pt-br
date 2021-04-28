---
description: IECTT (Internet Explorer Compatibility Test Tool)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: IECTT (Internet Explorer Compatibility Test Tool)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088280"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="16d8a-103">IECTT (Internet Explorer Compatibility Test Tool)</span><span class="sxs-lookup"><span data-stu-id="16d8a-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="16d8a-104">A ferramenta de teste de compatibilidade do Internet Explorer (IECTT) é um componente do [Kit de ferramentas de compatibilidade de aplicativos da Microsoft](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="16d8a-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="16d8a-105">Essa ferramenta pode ajudá-lo a diagnosticar problemas em seus aplicativos Web exibindo problemas em tempo real e, opcionalmente, carregando os resultados em um banco de dados ACT.</span><span class="sxs-lookup"><span data-stu-id="16d8a-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="16d8a-106">Os resultados incluem detalhes sobre possíveis problemas de compatibilidade e links para obter mais informações sobre cada problema de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="16d8a-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="16d8a-107">O IECTT também permite que você exclua problemas e modifique os atributos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="16d8a-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="16d8a-108">Para abrir o IECTT</span><span class="sxs-lookup"><span data-stu-id="16d8a-108">To open IECTT</span></span>

1.  <span data-ttu-id="16d8a-109">Instale o [Kit de ferramentas de compatibilidade de aplicativos da Microsoft](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="16d8a-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="16d8a-110">Clique em **Iniciar**, aponte para **programas**, aponte para kit de ferramentas de compatibilidade de **aplicativos da Microsoft 5,6**, aponte para ferramentas para **desenvolvedores e testadores** e clique em **ferramenta de teste de compatibilidade do Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="16d8a-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="16d8a-111">As seções a seguir descrevem cenários comuns de IECTT.</span><span class="sxs-lookup"><span data-stu-id="16d8a-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="16d8a-112">Exibir problemas em tempo real</span><span class="sxs-lookup"><span data-stu-id="16d8a-112">View Issues in Real Time</span></span>

<span data-ttu-id="16d8a-113">Você pode localizar e exibir seus problemas baseados na Web em tempo real, enquanto testa seus sites e aplicativos Web no Windows Internet Explorer 7 e no Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="16d8a-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="16d8a-114">Depois de concluir o teste, você poderá exibir os resultados na tela de **dados ao vivo** do IECTT.</span><span class="sxs-lookup"><span data-stu-id="16d8a-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="16d8a-115">Carregar problemas em seu banco de dados ACT</span><span class="sxs-lookup"><span data-stu-id="16d8a-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="16d8a-116">Você pode carregar seus problemas baseados na Web no banco de dados ACT, que processa as informações e permite que você exiba seus resultados na tela **analisar** do Gerenciador de compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="16d8a-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="16d8a-117">Coletar seus dados de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="16d8a-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="16d8a-118">Você pode coletar os dados de compatibilidade relacionados ao seu site e ao aplicativo Web usando a ferramenta IECTT com o Internet Explorer 7 ou o Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="16d8a-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="16d8a-119">**Para coletar os dados de compatibilidade**</span><span class="sxs-lookup"><span data-stu-id="16d8a-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="16d8a-120">Feche todas as janelas ativas do Internet Explorer do Windows.</span><span class="sxs-lookup"><span data-stu-id="16d8a-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="16d8a-121">No IECTT, na barra de ferramentas da **ferramenta de teste de compatibilidade do Internet Explorer** , clique em **habilitar**.</span><span class="sxs-lookup"><span data-stu-id="16d8a-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="16d8a-122">Abra uma janela do Internet Explorer 7 ou do Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="16d8a-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="16d8a-123">Uma mensagem é exibida e indica que o log de avaliação de compatibilidade está ativado.</span><span class="sxs-lookup"><span data-stu-id="16d8a-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="16d8a-124">Visite os sites ou aplicativos Web que são necessários para uso por sua organização.</span><span class="sxs-lookup"><span data-stu-id="16d8a-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="16d8a-125">À medida que você visita cada site, a ferramenta IECTT exibe, em tempo real, os possíveis problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="16d8a-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="16d8a-126">Na barra de ferramentas da **ferramenta de teste de compatibilidade do Internet Explorer** , clique em **desabilitar** quando terminar.</span><span class="sxs-lookup"><span data-stu-id="16d8a-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="16d8a-127">O processo de log de compatibilidade é concluído e interrompido.</span><span class="sxs-lookup"><span data-stu-id="16d8a-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="16d8a-128">Filtrar os resultados do problema</span><span class="sxs-lookup"><span data-stu-id="16d8a-128">Filter Your Issue Results</span></span>

<span data-ttu-id="16d8a-129">Você pode filtrar qualquer um dos resultados do IECTT por nome de objeto, por tipo de problema ou por ambos.</span><span class="sxs-lookup"><span data-stu-id="16d8a-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="16d8a-130">**Para filtrar os resultados do problema**</span><span class="sxs-lookup"><span data-stu-id="16d8a-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="16d8a-131">Na tela da **ferramenta de teste de compatibilidade do Internet Explorer** , clique em **Filtrar**.</span><span class="sxs-lookup"><span data-stu-id="16d8a-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="16d8a-132">A caixa de diálogo **filtro de problemas** é exibida.</span><span class="sxs-lookup"><span data-stu-id="16d8a-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="16d8a-133">Insira o nome do objeto que você pretende exibir na caixa **digite o nome do objeto para o qual exibir os problemas** .</span><span class="sxs-lookup"><span data-stu-id="16d8a-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="16d8a-134">Para obter mais informações sobre essa ferramenta e outras ferramentas de desenvolvedores, consulte o [que é a ferramenta de teste de compatibilidade do Internet Explorer?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) na biblioteca MSDN e a postagem [no blog log de compatibilidade de aplicativos no IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .</span><span class="sxs-lookup"><span data-stu-id="16d8a-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16d8a-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16d8a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16d8a-136">Ferramentas para depuração de aplicativos Web e Complementos</span><span class="sxs-lookup"><span data-stu-id="16d8a-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
