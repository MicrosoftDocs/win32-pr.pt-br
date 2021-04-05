---
description: Os modelos de Threading COM+ são projetados em uma coleção de objetos chamada Apartment. Um apartamento é uma coleção de contextos contidos em um processo.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelos de Threading COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103663694"
---
# <a name="com-threading-models"></a><span data-ttu-id="45ae8-104">Modelos de Threading COM+</span><span class="sxs-lookup"><span data-stu-id="45ae8-104">COM+ Threading Models</span></span>

<span data-ttu-id="45ae8-105">Os modelos de Threading COM+ são projetados em uma coleção de objetos chamada Apartment.</span><span class="sxs-lookup"><span data-stu-id="45ae8-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="45ae8-106">Um apartamento é uma coleção de contextos contidos em um processo, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="45ae8-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![Diagrama que mostra uma coleção de contextos em uma atividade, dentro de um apartamento, dentro de um processo.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="45ae8-108">Chamadas em um apartamento são diretas, enquanto chamadas entre Apartments (fora do processo) são indiretas e exigem código de proxy e stub.</span><span class="sxs-lookup"><span data-stu-id="45ae8-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="45ae8-109">Apartments permitem objetos com diferentes propriedades de sincronização e reentrância e têm duas categorias: thread único e multithread.</span><span class="sxs-lookup"><span data-stu-id="45ae8-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="45ae8-110">Os objetos em um STA (single-threaded apartment) são executados no thread específico em que foram criados.</span><span class="sxs-lookup"><span data-stu-id="45ae8-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="45ae8-111">STAs permite que apenas um método seja executado de cada vez.</span><span class="sxs-lookup"><span data-stu-id="45ae8-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="45ae8-112">Eles são projetados para interfaces do usuário e contam com a fila de mensagens do Microsoft Windows para processar chamadas de entrada.</span><span class="sxs-lookup"><span data-stu-id="45ae8-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="45ae8-113">Os objetos em um apartamento multithread (MTA) são executados em qualquer thread e permitem que qualquer número de métodos ocorra simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="45ae8-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="45ae8-114">MTAs dá suporte à reentrada implícita.</span><span class="sxs-lookup"><span data-stu-id="45ae8-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="45ae8-115">As classes COM+ são marcadas com uma propriedade **ThreadingModel** que permite que o com+ crie o objeto no apartamento apropriado.</span><span class="sxs-lookup"><span data-stu-id="45ae8-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="45ae8-116">Para determinar em qual apartamento um objeto é criado, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa a propriedade **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="45ae8-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="45ae8-117">Os threads devem chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) antes que possam usar com+.</span><span class="sxs-lookup"><span data-stu-id="45ae8-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="45ae8-118">Isso os cria dentro do apartamento e do contexto corretos.</span><span class="sxs-lookup"><span data-stu-id="45ae8-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="45ae8-119">O apartamento principal do thread é determinado como o primeiro STA chamado por **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="45ae8-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="45ae8-120">Isso geralmente é associado ao thread principal de um processo.</span><span class="sxs-lookup"><span data-stu-id="45ae8-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="45ae8-121">**CoInitializeEx** indica o tipo de apartamento exigido pelo thread definindo os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="45ae8-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="45ae8-122">**COinit \_ Multithread**– localiza o thread no único apartamento multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="45ae8-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="45ae8-123">**COinit \_ APARTMENTTHREADED**— coloca o thread em um novo Sta.</span><span class="sxs-lookup"><span data-stu-id="45ae8-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="45ae8-124">Os tópicos a seguir nesta seção fornecem mais informações sobre como usar modelos de threading e Apartments no COM+:</span><span class="sxs-lookup"><span data-stu-id="45ae8-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="45ae8-125">Atributo de modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="45ae8-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="45ae8-126">Apartments neutro</span><span class="sxs-lookup"><span data-stu-id="45ae8-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="45ae8-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45ae8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45ae8-128">Processos, threads e Apartments</span><span class="sxs-lookup"><span data-stu-id="45ae8-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="45ae8-129">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="45ae8-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
