---
description: Ativando filas de componentes
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Ativando filas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370417"
---
# <a name="activating-component-queues"></a><span data-ttu-id="d7d4b-103">Ativando filas de componentes</span><span class="sxs-lookup"><span data-stu-id="d7d4b-103">Activating Component Queues</span></span>

<span data-ttu-id="d7d4b-104">Fazer chamadas de método em um componente enfileirado não executa diretamente o método.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="d7d4b-105">Em vez disso, o [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) realiza marshaling e armazena chamadas de método e parâmetros em uma fila em que eles são recuperados e executados posteriormente pelo componente enfileirado.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="d7d4b-106">Ao contrário da ativação de um objeto DCOM remoto, o componente em fila não é instanciado quando um método é chamado.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="d7d4b-107">Essa é a ideia básica por trás do uso de componentes enfileirados – os componentes em fila não precisam ser instanciados ao mesmo tempo que o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="d7d4b-108">As descrições para ativar um aplicativo enfileirado pressupõem que o aplicativo está marcado como enfileirado e que a caixa de seleção do ouvinte está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="d7d4b-109">Você pode usar scripts para iniciar e parar um aplicativo enfileirado.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="d7d4b-110">Você pode colocar o script sob o controle do Agendador de tarefas para executá-lo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="d7d4b-111">Por exemplo, o script pode ser executado na reinicialização do sistema se os aplicativos estiverem permanentemente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="d7d4b-112">Se o aplicativo for processar transações no modo de lote, o script poderá ser executado em um determinado momento por dia em conjunto com um script de desligamento para garantir que o processamento em lotes seja interrompido em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="d7d4b-113">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="d7d4b-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="d7d4b-114">Para iniciar um aplicativo em fila, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d7d4b-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="d7d4b-115">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="d7d4b-116">Clique com o botão direito do mouse no aplicativo cuja fila você deseja ativar.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="d7d4b-117">Clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="d7d4b-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d7d4b-118">Visual Basic</span></span>

<span data-ttu-id="d7d4b-119">Consulte o exemplo COMAdminCatalog. StartApplication.</span><span class="sxs-lookup"><span data-stu-id="d7d4b-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="d7d4b-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="d7d4b-120">C/C++</span></span>

<span data-ttu-id="d7d4b-121">Consulte o exemplo [**ICOMAdminCatalog:: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .</span><span class="sxs-lookup"><span data-stu-id="d7d4b-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7d4b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7d4b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7d4b-123">Usando o moniker da fila</span><span class="sxs-lookup"><span data-stu-id="d7d4b-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



