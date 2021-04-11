---
description: Você pode monitorar as estatísticas de objeto conforme um aplicativo é executado. Ao fazer isso, você pode ajustar as características do pool de objetos para obter o equilíbrio entre o desempenho e os recursos que gostaria de ter.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Estatísticas de objeto de monitoramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296089"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="3a67e-104">Estatísticas de objeto de monitoramento</span><span class="sxs-lookup"><span data-stu-id="3a67e-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="3a67e-105">Você pode monitorar as estatísticas de objeto conforme um aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="3a67e-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="3a67e-106">Ao fazer isso, você pode ajustar as características do pool de objetos para obter o equilíbrio entre o desempenho e os recursos que gostaria de ter.</span><span class="sxs-lookup"><span data-stu-id="3a67e-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="3a67e-107">Você pode monitorar o status de todos os objetos que estão configurados para dar suporte a estatísticas de objetos e relatórios de eventos.</span><span class="sxs-lookup"><span data-stu-id="3a67e-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="3a67e-108">A habilitação de estatísticas de objeto tem uma sobrecarga de desempenho muito pequena.</span><span class="sxs-lookup"><span data-stu-id="3a67e-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="3a67e-109">**Para habilitar estatísticas de objeto**</span><span class="sxs-lookup"><span data-stu-id="3a67e-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="3a67e-110">No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="3a67e-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="3a67e-111">Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="3a67e-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="3a67e-112">Para habilitar as estatísticas de objeto para o componente, em **contexto de ativação**, marque a caixa de seleção o **componente dá suporte a eventos e estatísticas** .</span><span class="sxs-lookup"><span data-stu-id="3a67e-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="3a67e-113">**Para monitorar o status do objeto**</span><span class="sxs-lookup"><span data-stu-id="3a67e-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="3a67e-114">Na árvore de console da ferramenta administrativa serviços de componentes, abra a pasta do aplicativo que inclui os componentes que você deseja monitorar.</span><span class="sxs-lookup"><span data-stu-id="3a67e-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="3a67e-115">Clique com o botão direito do mouse na pasta **componentes** , aponte para **Exibir** e clique em **modo de exibição de status**.</span><span class="sxs-lookup"><span data-stu-id="3a67e-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="3a67e-116">O painel de detalhes agora exibe a exibição de status de todos os componentes no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a67e-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="3a67e-117">A tabela a seguir descreve as seis colunas no modo de exibição de status.</span><span class="sxs-lookup"><span data-stu-id="3a67e-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="3a67e-118">Coluna</span><span class="sxs-lookup"><span data-stu-id="3a67e-118">Column</span></span>                        | <span data-ttu-id="3a67e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a67e-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="3a67e-120">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="3a67e-120">**ProgID**</span></span><br/>         | <span data-ttu-id="3a67e-121">Identifica um componente específico.</span><span class="sxs-lookup"><span data-stu-id="3a67e-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="3a67e-122">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="3a67e-122">**Objects**</span></span><br/>        | <span data-ttu-id="3a67e-123">Mostra o número de objetos que estão sendo mantidos por referências de cliente.</span><span class="sxs-lookup"><span data-stu-id="3a67e-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="3a67e-124">**Ativado**</span><span class="sxs-lookup"><span data-stu-id="3a67e-124">**Activated**</span></span><br/>      | <span data-ttu-id="3a67e-125">Mostra o número de objetos que estão ativados no momento.</span><span class="sxs-lookup"><span data-stu-id="3a67e-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="3a67e-126">**Em pool**</span><span class="sxs-lookup"><span data-stu-id="3a67e-126">**Pooled**</span></span><br/>         | <span data-ttu-id="3a67e-127">Mostra o número total de objetos criados pelo pool, incluindo objetos que estão em uso e objetos que são desativados.</span><span class="sxs-lookup"><span data-stu-id="3a67e-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="3a67e-128">**Em chamada**</span><span class="sxs-lookup"><span data-stu-id="3a67e-128">**In Call**</span></span><br/>        | <span data-ttu-id="3a67e-129">Identifica objetos em chamada.</span><span class="sxs-lookup"><span data-stu-id="3a67e-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="3a67e-130">**Tempo de chamada (MS)**</span><span class="sxs-lookup"><span data-stu-id="3a67e-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="3a67e-131">Mostra a duração média da chamada (em milissegundos) das chamadas de método feitas nos últimos 20 segundos (até 20 chamadas).</span><span class="sxs-lookup"><span data-stu-id="3a67e-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="3a67e-132">O tempo de chamada é medido no objeto e não inclui o tempo usado para atravessar a rede.</span><span class="sxs-lookup"><span data-stu-id="3a67e-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="3a67e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a67e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a67e-134">Configurando um componente a ser agrupado</span><span class="sxs-lookup"><span data-stu-id="3a67e-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




