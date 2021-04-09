---
description: .
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Ferramentas de desenvolvimento do Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a184b513717655ee0a738be6318b4c8f2515ca3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091710"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="9b492-103">Ferramentas de desenvolvimento do Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="9b492-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="9b492-104">O Windows Internet Explorer 8 inclui o recurso Ferramentas para Desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="9b492-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="9b492-105">Esse recurso permite que você depure o Microsoft JScript rapidamente, investigue um comportamento específico do Windows Internet Explorer ou itere rapidamente para criar um protótipo ou testar uma nova solução de design.</span><span class="sxs-lookup"><span data-stu-id="9b492-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="9b492-106">As seções a seguir descrevem as características importantes do Ferramentas para Desenvolvedores no Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9b492-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="9b492-107">Integrado e simples de usar</span><span class="sxs-lookup"><span data-stu-id="9b492-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="9b492-108">Os Ferramentas para Desenvolvedores estão incluídos em todas as instalações do Internet Explorer 8, para que você possa depurar problemas em qualquer computador que esteja executando o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9b492-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="9b492-109">Além disso, as ferramentas são carregadas somente quando você precisa delas para limitar como elas afetam o desempenho do navegador.</span><span class="sxs-lookup"><span data-stu-id="9b492-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="9b492-110">Usando o Ferramentas para Desenvolvedores, você pode depurar rapidamente apenas o processo atual do Internet Explorer, em vez de Depurar para todo o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9b492-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="9b492-111">Fornecer uma interface visual para a plataforma</span><span class="sxs-lookup"><span data-stu-id="9b492-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="9b492-112">Em vez de fazer a engenharia reversa de como seu site funciona ou modificar seu site para gerar informações de depuração, o Ferramentas para Desenvolvedores permite que você examine o Internet Explorer para exibir sua representação do seu site.</span><span class="sxs-lookup"><span data-stu-id="9b492-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="9b492-113">Essa exibição reduz o tempo gasto na depuração de sites dinâmicos, em que a inspeção de origem não é útil ou investiga um comportamento específico do Internet Explorer, no qual uma ferramenta de criação genérica não pode ajudar.</span><span class="sxs-lookup"><span data-stu-id="9b492-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="9b492-114">Habilitar experimentação rápida</span><span class="sxs-lookup"><span data-stu-id="9b492-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="9b492-115">Ao criar um protótipo de um novo design ou correções de teste nas versões anteriores do Internet Explorer, é provável que você edite sua origem, salve-a, atualize sua página no navegador e repita.</span><span class="sxs-lookup"><span data-stu-id="9b492-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="9b492-116">O Ferramentas para Desenvolvedores simplificar esse cenário permitindo que você edite seu site no navegador e veja as alterações imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9b492-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="9b492-117">Otimizar o desempenho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="9b492-117">Optimize Application Performance</span></span>

<span data-ttu-id="9b492-118">Para identificar e corrigir problemas de desempenho, é provável que você itere concentrando-se em um cenário por vez.</span><span class="sxs-lookup"><span data-stu-id="9b492-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="9b492-119">Usando o criador de perfil de script no Ferramentas para Desenvolvedores, você pode coletar estatísticas, incluindo o tempo de execução e o número de vezes que uma função JavaScript é chamada.</span><span class="sxs-lookup"><span data-stu-id="9b492-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="9b492-120">Você pode usar essas informações ao testar seu aplicativo e usar o relatório de perfil para identificar e corrigir gargalos de desempenho rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9b492-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="9b492-121">Para acessar o Ferramentas para Desenvolvedores, pressione F12 enquanto estiver exibindo uma página da Web ou clique em **ferramentas para desenvolvedores** no menu **ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="9b492-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b492-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b492-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b492-123">Ferramentas para depuração de aplicativos Web e Complementos</span><span class="sxs-lookup"><span data-stu-id="9b492-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



