---
description: Inicialização e recuperação do CRM do COM+
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicialização e recuperação do CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771289"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="933d1-103">Inicialização e recuperação do CRM do COM+</span><span class="sxs-lookup"><span data-stu-id="933d1-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="933d1-104">Se um aplicativo de servidor tiver a caixa de seleção **habilitar gerenciadores de recursos de compensação** selecionada (usando a ferramenta administrativa serviços de componentes, na guia **avançado** da página de propriedades do aplicativo com+), na primeira vez que ele for iniciado, ele criará um arquivo de log do CRM a ser usado por todos os CRMS nesse processo de aplicativo do servidor.</span><span class="sxs-lookup"><span data-stu-id="933d1-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="933d1-105">(Para obter instruções detalhadas sobre como configurar o CRM, consulte [Configurando componentes do com+ CRM](configuring-com--crm-components.md).)</span><span class="sxs-lookup"><span data-stu-id="933d1-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="933d1-106">O nome do arquivo de log do CRM criado para o aplicativo de servidor é baseado na AppId (um GUID) do aplicativo de servidor e o arquivo de log do CRM é colocado no mesmo diretório que o arquivo de log do DTC (normalmente seu diretório% SystemRoot% \\ WinNT \\ System32 \\ DtcLog).</span><span class="sxs-lookup"><span data-stu-id="933d1-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="933d1-107">Os arquivos de log do CRM têm a extensão. crmlog.</span><span class="sxs-lookup"><span data-stu-id="933d1-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="933d1-108">Pode ser necessário alterar o local padrão de um arquivo de log do CRM devido a motivos de desempenho (para ter o arquivo de log do DTC em um disco diferente do arquivo de log do CRM) ou talvez devido ao uso do CRM em um ambiente de cluster.</span><span class="sxs-lookup"><span data-stu-id="933d1-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="933d1-109">O local dos arquivos de log do CRM pode ser alterado usando o SDK de administração do COM+.</span><span class="sxs-lookup"><span data-stu-id="933d1-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="933d1-110">O nome da propriedade é CRMLogFile e existe no objeto da coleção [**Applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="933d1-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="933d1-111">Quando um aplicativo de servidor (que está habilitado para CRM) é iniciado e descobre que um arquivo de log do CRM já existe para esse aplicativo de servidor, ele executa a recuperação nesse arquivo de log do CRM.</span><span class="sxs-lookup"><span data-stu-id="933d1-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="933d1-112">A *recuperação* é o processo de concluir todas as transações que foram interrompidas por uma falha e envolve a infraestrutura de CRM lendo o arquivo de log do CRM para quaisquer transações que não foram totalmente concluídas.</span><span class="sxs-lookup"><span data-stu-id="933d1-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="933d1-113">Se ele encontrar algum, ele entrará em contato com o DTC para determinar o resultado da transação.</span><span class="sxs-lookup"><span data-stu-id="933d1-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="933d1-114">Em seguida, ele cria o compensador de CRM e passa as notificações de confirmação ou anulação conforme necessário, junto com os registros de log associados.</span><span class="sxs-lookup"><span data-stu-id="933d1-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="933d1-115">As notificações de preparação não são recebidas pelo compensador de CRM durante a recuperação.</span><span class="sxs-lookup"><span data-stu-id="933d1-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="933d1-116">O compensador de CRM tem um sinalizador para distinguir se ele está sendo chamado durante a operação normal ou durante a recuperação.</span><span class="sxs-lookup"><span data-stu-id="933d1-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="933d1-117">A recuperação normalmente localizará as transações não concluídas somente se o aplicativo do servidor tiver sido desligado de forma anormal, devido a uma falha de processo do aplicativo do servidor ou uma falha do computador.</span><span class="sxs-lookup"><span data-stu-id="933d1-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="933d1-118">Se o aplicativo do servidor tiver permissão para desligar normalmente, devido ao tempo limite ocioso ou ao desligamento manual por meio da ferramenta administrativa serviços de componentes, o arquivo de log será limpo.</span><span class="sxs-lookup"><span data-stu-id="933d1-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="933d1-119">O início de um aplicativo do servidor CRM para recuperação não é iniciado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="933d1-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="933d1-120">Algumas ações externas devem ser executadas para iniciar o aplicativo do servidor de CRM em que a recuperação é necessária.</span><span class="sxs-lookup"><span data-stu-id="933d1-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="933d1-121">Normalmente, isso seria criar um componente nesse aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="933d1-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="933d1-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="933d1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="933d1-123">Conceitos do Gerenciador de recursos de compensação COM+</span><span class="sxs-lookup"><span data-stu-id="933d1-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="933d1-124">Processo operacional de CRM do COM+</span><span class="sxs-lookup"><span data-stu-id="933d1-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



