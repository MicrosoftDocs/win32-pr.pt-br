---
description: O SDK do Monitor de Rede inclui as funções e o código de exemplo que você precisa para criar especialistas. No entanto, você também pode usar as ferramentas existentes, incluindo um editor de caixa de diálogo.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091527"
---
# <a name="programming-an-expert"></a><span data-ttu-id="0929b-104">Programando um especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-104">Programming an Expert</span></span>

<span data-ttu-id="0929b-105">O SDK do Monitor de Rede inclui as funções e o código de exemplo que você precisa para criar especialistas.</span><span class="sxs-lookup"><span data-stu-id="0929b-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="0929b-106">No entanto, você também pode usar as ferramentas existentes, incluindo um editor de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0929b-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="0929b-107">Requisitos mínimos para executar um especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="0929b-108">A tabela a seguir lista os pontos de entrada da DLL e as funções de especialista que você deve usar para criar um especialista.</span><span class="sxs-lookup"><span data-stu-id="0929b-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="0929b-109">Nome</span><span class="sxs-lookup"><span data-stu-id="0929b-109">Name</span></span>                                                 | <span data-ttu-id="0929b-110">Type</span><span class="sxs-lookup"><span data-stu-id="0929b-110">Type</span></span>               | <span data-ttu-id="0929b-111">Obrigatório?</span><span class="sxs-lookup"><span data-stu-id="0929b-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="0929b-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="0929b-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="0929b-113">Função de entrada de DLL</span><span class="sxs-lookup"><span data-stu-id="0929b-113">DLL entry function</span></span> | <span data-ttu-id="0929b-114">Sim</span><span class="sxs-lookup"><span data-stu-id="0929b-114">Yes</span></span>                                             |
| [<span data-ttu-id="0929b-115">**Registrar especialista**</span><span class="sxs-lookup"><span data-stu-id="0929b-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="0929b-116">Função de entrada de DLL</span><span class="sxs-lookup"><span data-stu-id="0929b-116">DLL entry function</span></span> | <span data-ttu-id="0929b-117">Sim</span><span class="sxs-lookup"><span data-stu-id="0929b-117">Yes</span></span>                                             |
| [<span data-ttu-id="0929b-118">**Executar**</span><span class="sxs-lookup"><span data-stu-id="0929b-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="0929b-119">Função de entrada de DLL</span><span class="sxs-lookup"><span data-stu-id="0929b-119">DLL entry function</span></span> | <span data-ttu-id="0929b-120">Sim</span><span class="sxs-lookup"><span data-stu-id="0929b-120">Yes</span></span>                                             |
| [<span data-ttu-id="0929b-121">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="0929b-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="0929b-122">Função de entrada de DLL</span><span class="sxs-lookup"><span data-stu-id="0929b-122">DLL entry function</span></span> | <span data-ttu-id="0929b-123">Somente se o especialista fornecer a configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="0929b-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="0929b-124">**ExpertIndicateStatus**</span><span class="sxs-lookup"><span data-stu-id="0929b-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="0929b-125">Função de especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-125">Expert function</span></span>    | <span data-ttu-id="0929b-126">Sim</span><span class="sxs-lookup"><span data-stu-id="0929b-126">Yes</span></span>                                             |
| [<span data-ttu-id="0929b-127">**ExpertSubmitEvent**</span><span class="sxs-lookup"><span data-stu-id="0929b-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="0929b-128">Função de especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-128">Expert function</span></span>    | <span data-ttu-id="0929b-129">Sim</span><span class="sxs-lookup"><span data-stu-id="0929b-129">Yes</span></span>                                             |



 

<span data-ttu-id="0929b-130">Examine os tópicos de referência do Expert e do parser no SDK do Monitor de Rede para atualizar seu código-fonte e, em seguida, use o código de exemplo e os procedimentos fornecidos nestes tópicos:</span><span class="sxs-lookup"><span data-stu-id="0929b-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="0929b-131">Criando um especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="0929b-132">Instalando um especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="0929b-133">Depurando um especialista</span><span class="sxs-lookup"><span data-stu-id="0929b-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="0929b-134">As DLLs de especialistas exigem o C, não o C++, a Convenção de chamada porque as funções são chamadas por meio de ponteiros de função usando uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="0929b-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="0929b-135">Por meio de um conjunto de funções especialistas especializadas, o especialista tem acesso aos quadros na captura.</span><span class="sxs-lookup"><span data-stu-id="0929b-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="0929b-136">O especialista pode usar a maior parte da API de Monitor de Rede para manipular os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="0929b-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="0929b-137">Quando um especialista encontra informações para enviar ao usuário, ele empacota as informações em uma estrutura de dados de evento e a envia para Monitor de Rede, que, em seguida, exibe as informações em uma janela de saída de especialista.</span><span class="sxs-lookup"><span data-stu-id="0929b-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="0929b-138">O especialista deve atualizar periodicamente Monitor de Rede com informações de status de conclusão de porcentagem, que é fornecida pela função [**ExpertIndicateStatus**](expertindicatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="0929b-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="0929b-139">As funções exportadas do especialista são chamadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0929b-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="0929b-140">Quando Monitor de Rede está criando a lista de especialistas para apresentar ao usuário, Monitor de Rede chama a função de [**especialista de registro**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="0929b-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="0929b-141">Após a chamada para o **registro**, se o especialista for configurável, monitor de rede chamará a função [**Configurar**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="0929b-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="0929b-142">Quando o usuário Monitor de Rede clica em **executar especialista**, monitor de rede chama a função [**executar**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="0929b-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="0929b-143">Quando os especialistas analisam os quadros solicitados e encontram um problema, eles usam o [**ExpertSubmitEvent**](expertsubmitevent.md) para enviar um evento que contém informações sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="0929b-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="0929b-144">Monitor de Rede distribui o evento para o Visualizador de Eventos padrão (compartilhado) ou (se o especialista o registra) em uma Visualizador de Eventos privada.</span><span class="sxs-lookup"><span data-stu-id="0929b-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



