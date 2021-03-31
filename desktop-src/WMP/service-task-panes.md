---
title: Painéis de tarefas de serviço
description: Painéis de tarefas de serviço
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Lojas online do Windows Media Player, painéis de tarefas de serviço
- lojas online, painéis de tarefas de serviço
- Digite 2 lojas online, painéis de tarefas de serviço
- Repositórios online do Windows Media Player, painéis de tarefas
- lojas online, painéis de tarefas
- Digite 2 lojas online, painéis de tarefas
- Windows Media Player, painéis de tarefas de serviço
- Windows Media Player, painéis de tarefas
- painéis de tarefas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005664"
---
# <a name="service-task-panes"></a><span data-ttu-id="9528d-112">Painéis de tarefas de serviço</span><span class="sxs-lookup"><span data-stu-id="9528d-112">Service Task Panes</span></span>

<span data-ttu-id="9528d-113">No Windows Media Player 10, os provedores de loja online podem configurar o Windows Media Player para exibir até três painéis de tarefas, chamados painéis de tarefas de serviço.</span><span class="sxs-lookup"><span data-stu-id="9528d-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="9528d-114">Cada painel de tarefas de serviço é representado por um botão personalizável que o Windows Media Player exibe no lado direito da barra de tarefas de recursos.</span><span class="sxs-lookup"><span data-stu-id="9528d-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="9528d-115">Cada painel de tarefas de serviço hospeda uma página da Web que é a interface do usuário para um recurso de loja online específico. A aparência dos painéis de tarefas de serviço é definida pelo documento XML serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="9528d-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="9528d-116">Neste documento, os painéis de tarefas de serviço são representados por três elementos: **ServiceTask1**, **ServiceTask2** e **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="9528d-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="9528d-117">Esses painéis de tarefas de serviço têm a finalidade de fornecer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9528d-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="9528d-118">Um serviço de música.</span><span class="sxs-lookup"><span data-stu-id="9528d-118">A music service.</span></span>
-   <span data-ttu-id="9528d-119">Um serviço de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9528d-119">A video service.</span></span>
-   <span data-ttu-id="9528d-120">Um serviço de rádio.</span><span class="sxs-lookup"><span data-stu-id="9528d-120">A radio service.</span></span>

<span data-ttu-id="9528d-121">Você pode posicionar esses recursos no Windows Media Player em qualquer ordem que desejar, mas o **ServiceTask1** deve ser o painel de tarefas principal para envolver atividades comerciais.</span><span class="sxs-lookup"><span data-stu-id="9528d-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="9528d-122">A página da web hospedada em cada painel de tarefas de serviço tem acesso ao objeto **externo** .</span><span class="sxs-lookup"><span data-stu-id="9528d-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="9528d-123">Esse objeto fornece métodos, propriedades e um evento que fornecem funcionalidade especial para páginas da Web no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9528d-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="9528d-124">Por exemplo, você pode usar o evento e as propriedades de **externo** para fazer com que a aparência da página da Web corresponda ao esquema de cores escolhido pelo usuário para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9528d-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="9528d-125">No Windows Media Player 11, não há painéis de tarefas de serviço.</span><span class="sxs-lookup"><span data-stu-id="9528d-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="9528d-126">Em vez disso, há uma única guia **repositórios online** , que hospeda a página da Web principal para o repositório online ativo.</span><span class="sxs-lookup"><span data-stu-id="9528d-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="9528d-127">No documento do serviceInfo, a guia **lojas online** é representada pelo elemento **ServiceTask1** ; os elementos **ServiceTask2** e **ServiceTask3** são ignorados.</span><span class="sxs-lookup"><span data-stu-id="9528d-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9528d-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9528d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9528d-129">**Sobre as lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9528d-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9528d-130">**Objeto externo para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9528d-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9528d-131">**Documento do serviceInfo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9528d-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




