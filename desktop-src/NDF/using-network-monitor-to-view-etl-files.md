---
title: Uso do Monitor de Rede para exibição de arquivos ETL
description: Monitor de Rede 3,3 permite que os usuários analisem, filtrem e exibam um arquivo ETL (usando o Windows Vista ou posterior).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103923022"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="9c141-103">Uso do Monitor de Rede para exibição de arquivos ETL</span><span class="sxs-lookup"><span data-stu-id="9c141-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="9c141-104">[Monitor de Rede 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permite que os usuários analisem, filtrem e exibam um arquivo ETL (usando o Windows Vista ou posterior).</span><span class="sxs-lookup"><span data-stu-id="9c141-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="9c141-105">(Se estiver usando o Monitor de Rede 3,2, você precisará baixar e instalar analisadores adicionais do [codeplex](https://www.codeplex.com/NMParsers) para renderizar os eventos de rastreamento de rede.)</span><span class="sxs-lookup"><span data-stu-id="9c141-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="9c141-106">Os arquivos ETL correlacionados agrupam os eventos relevantes juntos.</span><span class="sxs-lookup"><span data-stu-id="9c141-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="9c141-107">O illlustration abaixo mostra um arquivo correlacionado aberto no Monitor de Rede, com a conversa habilitada.</span><span class="sxs-lookup"><span data-stu-id="9c141-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![Captura de tela que mostra a Monitor de Rede, com eventos correlacionados realçados na janela esquerda e UTEvent realçados na lista suspensa.](images/ut-netmon1.png)

<span data-ttu-id="9c141-109">Os eventos correlacionados são agrupados por atividade no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="9c141-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="9c141-110">Você pode selecionar um evento no painel Resumo do quadro e clicar com o botão direito do mouse para selecionar a conversa no nível do evento de rede.</span><span class="sxs-lookup"><span data-stu-id="9c141-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="9c141-111">Isso exibirá uma atividade relacionada no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="9c141-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="9c141-112">Selecionar uma atividade específica no painel esquerdo e expandi-la mostrará a lista de provedores para os eventos correlacionados.</span><span class="sxs-lookup"><span data-stu-id="9c141-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![Captura de tela que mostra a Monitor de Rede com uma atividade selecionada no painel esquerdo e eventos correspondentes a esse evento no painel direito.](images/ut-netmon2.png)

<span data-ttu-id="9c141-114">Quando você seleciona um provedor específico no painel esquerdo, uma lista de eventos específicos para esse provedor e atividade será exibida no painel Resumo do quadro.</span><span class="sxs-lookup"><span data-stu-id="9c141-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![Captura de tela que mostra um provedor específico selecionado no painel esquerdo e uma lista de eventos específicos para o provedor realçado no painel superior direito.](images/ut-netmon3.png)

<span data-ttu-id="9c141-116">Os filtros podem ser aplicados no Monitor de Rede para facilitar a exibição e a localização dos eventos ou do pacote corretos.</span><span class="sxs-lookup"><span data-stu-id="9c141-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="9c141-117">Por exemplo, você pode aplicar um filtro aos eventos de erro selecionados (por exemplo, **UTEvent. Header. Descriptor. Level = = 2**) para exibi-los em uma determinada cor.</span><span class="sxs-lookup"><span data-stu-id="9c141-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![Captura de tela que mostra a caixa de diálogo ' Editar Filtro de cores '.](images/ut-netmon4.png)

<span data-ttu-id="9c141-119">Os filtros também podem ser aplicados para marcar provedores diferentes em cores diferentes, de modo que os resultados sejam mais fáceis de exibir.</span><span class="sxs-lookup"><span data-stu-id="9c141-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![Captura de tela que mostra um exemplo de provedores diferentes marcados em cores diferentes.](images/ut-netmon5.png)

<span data-ttu-id="9c141-121">Para aplicar um filtro, clique em **ColorFilters** no menu **filtros** .</span><span class="sxs-lookup"><span data-stu-id="9c141-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="9c141-122">A tabela a seguir mostra alguns exemplos de filtros úteis.</span><span class="sxs-lookup"><span data-stu-id="9c141-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="9c141-123">Filtrar</span><span class="sxs-lookup"><span data-stu-id="9c141-123">Filter</span></span>                                                                        | <span data-ttu-id="9c141-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c141-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9c141-125">UTEvent. Header. Descriptor. nível = = 2</span><span class="sxs-lookup"><span data-stu-id="9c141-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="9c141-126">Filtra somente eventos de erro.</span><span class="sxs-lookup"><span data-stu-id="9c141-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="9c141-127">UTEvent. Header. Descriptor. nível = = 3</span><span class="sxs-lookup"><span data-stu-id="9c141-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="9c141-128">Filtra somente eventos de aviso.</span><span class="sxs-lookup"><span data-stu-id="9c141-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="9c141-129">UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="9c141-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="9c141-130">Filtra somente eventos com a ID de evento 2001.</span><span class="sxs-lookup"><span data-stu-id="9c141-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="9c141-131">\_MICROSOFTWINDOWSWLANAUTOCONFIG WLAN</span><span class="sxs-lookup"><span data-stu-id="9c141-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="9c141-132">Filtra somente os eventos do serviço WLAN.</span><span class="sxs-lookup"><span data-stu-id="9c141-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="9c141-133">N802 \_ MicrosoftWindowsNWiFi</span><span class="sxs-lookup"><span data-stu-id="9c141-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="9c141-134">Filtra somente os eventos do driver WiFi nativo.</span><span class="sxs-lookup"><span data-stu-id="9c141-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="9c141-135">WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG e UTEvent.Header.Descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="9c141-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="9c141-136">Filtra somente eventos com a ID de evento 2001 emitida do serviço de WLAN.</span><span class="sxs-lookup"><span data-stu-id="9c141-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




