---
description: Um aplicativo que contém pelo menos um componente queuable pode ser marcado como enfileirado usando a ferramenta administrativa serviços de componentes.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Criando filas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811613"
---
# <a name="creating-component-queues"></a><span data-ttu-id="fd3c4-103">Criando filas de componentes</span><span class="sxs-lookup"><span data-stu-id="fd3c4-103">Creating Component Queues</span></span>

<span data-ttu-id="fd3c4-104">Um aplicativo que contém pelo menos um componente queuable pode ser marcado como enfileirado usando a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="fd3c4-105">Quando um aplicativo é marcado como enfileirado, o COM+ cria automaticamente uma fila de enfileiramento de mensagens para ele.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="fd3c4-106">O nome da fila é o nome do aplicativo; Se o nome da fila corresponder ao nome de uma fila existente, o COM+ usará a fila existente.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="fd3c4-107">O parâmetro do nome do *caminho* do serviço de enfileiramento de mensagens é uma combinação do RSN (Remote Server Name) e do nome do aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="fd3c4-108">O RSN refere-se ao destino de uma ativação remota.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="fd3c4-109">Você especifica um RSN durante a instalação de um aplicativo exportável do cliente em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="fd3c4-110">O procedimento de instalação usa o RSN para direcionar a ativação para um computador cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="fd3c4-111">Para obter mais informações sobre nomes de fila, consulte a tabela de parâmetros na seção "parâmetros do moniker da fila" em [usando o moniker da fila](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="fd3c4-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="fd3c4-112">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="fd3c4-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="fd3c4-113">Para especificar um aplicativo COM+ como enfileirado, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fd3c4-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="fd3c4-114">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="fd3c4-115">Clique com o botão direito do mouse no aplicativo para o qual você deseja criar uma fila e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="fd3c4-116">Selecione a guia **enfileiramento** na caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="fd3c4-117">Ative a caixa de seleção rotulada **na fila – esse aplicativo pode ser** acessado pelas filas do MSMQ.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="fd3c4-118">Se a caixa de seleção **na fila** estiver esmaecida, o aplicativo não conterá nenhum componente queuable.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="fd3c4-119">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="fd3c4-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fd3c4-120">Visual Basic</span></span>

<span data-ttu-id="fd3c4-121">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="fd3c4-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="fd3c4-122">C/C++</span></span>

<span data-ttu-id="fd3c4-123">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3c4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd3c4-124">Remarks</span></span>

<span data-ttu-id="fd3c4-125">As filas criadas pela biblioteca de administração COM+ ou pela ferramenta administrativa serviços de componentes são marcadas com o atributo transacional do enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="fd3c4-126">Depois que um aplicativo enfileirado é instalado no servidor, ele pode ser disponibilizado para clientes exportando o aplicativo e, em seguida, importando o aplicativo em cada cliente.</span><span class="sxs-lookup"><span data-stu-id="fd3c4-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd3c4-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd3c4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd3c4-128">Criando componentes do Queuable</span><span class="sxs-lookup"><span data-stu-id="fd3c4-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="fd3c4-129">Arquitetura de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="fd3c4-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



