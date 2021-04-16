---
description: Implantando para comunicação mais rápida
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Implantando para comunicação mais rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787020"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="f3634-103">Implantando para comunicação mais rápida</span><span class="sxs-lookup"><span data-stu-id="f3634-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="f3634-104">O desempenho é uma consideração importante ao implantar um aplicativo COM+, e o local do componente é a chave para obter o melhor desempenho de um aplicativo bem projetado.</span><span class="sxs-lookup"><span data-stu-id="f3634-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="f3634-105">Uma vez amplamente ocupou isso com arquiteturas escalonáveis de aplicativos, o desempenho poderia ser resolvido simplesmente movendo os componentes primários do aplicativo para um hardware mais rápido.</span><span class="sxs-lookup"><span data-stu-id="f3634-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="f3634-106">Isso provou não ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="f3634-106">This has proven not to be true.</span></span> <span data-ttu-id="f3634-107">Os problemas de desempenho não surgem do desempenho de componentes individuais, mas dos links Conectando componentes.</span><span class="sxs-lookup"><span data-stu-id="f3634-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="f3634-108">O fator primário para o sucesso é o local.</span><span class="sxs-lookup"><span data-stu-id="f3634-108">The primary factor for success is location.</span></span> <span data-ttu-id="f3634-109">A proximidade ou o local físico, o tempo, a capacidade e a finalidade são aspectos distintos do local que se aplicam à implantação de um aplicativo do COM+, todos os quais afetam o desempenho.</span><span class="sxs-lookup"><span data-stu-id="f3634-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="f3634-110">O melhor desempenho é quando os componentes e os recursos do aplicativo são projetados e implantados para corresponder às demandas colocadas sobre eles pela carga de trabalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f3634-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="f3634-111">Em geral, você deve implantar componentes para minimizar a comunicação entre processos e, especialmente entre computadores, entre componentes.</span><span class="sxs-lookup"><span data-stu-id="f3634-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="f3634-112">Se o design do seu aplicativo for eficiente, as classes dentro de um componente serão agrupadas por uso e função para maximizar a comunicação nos componentes.</span><span class="sxs-lookup"><span data-stu-id="f3634-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="f3634-113">Na implantação de componentes, você precisa garantir que os componentes estejam localizados logicamente para usar as relações entre os componentes e para reduzir a quantidade de mensagens entre os componentes.</span><span class="sxs-lookup"><span data-stu-id="f3634-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3634-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3634-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3634-115">Projetando para implantação</span><span class="sxs-lookup"><span data-stu-id="f3634-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



