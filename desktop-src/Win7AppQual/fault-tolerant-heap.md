---
description: Heap tolerante a falhas
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Heap tolerante a falhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088394"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="96348-103">Heap tolerante a falhas</span><span class="sxs-lookup"><span data-stu-id="96348-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="96348-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="96348-104">Affected Platforms</span></span>

<span data-ttu-id="96348-105">**Clientes-** Windows 7</span><span class="sxs-lookup"><span data-stu-id="96348-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="96348-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="96348-106">Feature Impact</span></span>

 <span data-ttu-id="96348-107">**Severidade-** Médio</span><span class="sxs-lookup"><span data-stu-id="96348-107">**Severity -** Medium</span></span>  
<span data-ttu-id="96348-108">**Frequência-** Pequena</span><span class="sxs-lookup"><span data-stu-id="96348-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="96348-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="96348-109">Description</span></span>

<span data-ttu-id="96348-110">O FTH (heap tolerante a falhas) é um subsistema do Windows 7 responsável por monitorar falhas do aplicativo e aplicar mitigações de forma autônoma para evitar falhas futuras por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96348-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="96348-111">Para a grande maioria dos usuários, o FTH funcionará sem a necessidade de intervenção ou alteração em sua parte.</span><span class="sxs-lookup"><span data-stu-id="96348-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="96348-112">No entanto, em alguns casos, os desenvolvedores de aplicativos e os testadores de software podem precisar substituir o comportamento padrão desse sistema.</span><span class="sxs-lookup"><span data-stu-id="96348-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="96348-113">Solução</span><span class="sxs-lookup"><span data-stu-id="96348-113">Solution</span></span>

<span data-ttu-id="96348-114">**Exibindo a atividade de heap tolerante a falhas**</span><span class="sxs-lookup"><span data-stu-id="96348-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="96348-115">O heap tolerante a falhas registra informações quando o serviço é iniciado, interrompe ou começa a atenuar problemas de um novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96348-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="96348-116">Para exibir essas informações, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="96348-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="96348-117">Clique no menu Iniciar.</span><span class="sxs-lookup"><span data-stu-id="96348-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="96348-118">Clique com o botão direito do mouse em **computador** e clique em **gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="96348-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="96348-119">Clique em **Visualizador de eventos**  >  **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows > tolerância a falhas-heap**</span><span class="sxs-lookup"><span data-stu-id="96348-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="96348-120">Exibir eventos de FTH.</span><span class="sxs-lookup"><span data-stu-id="96348-120">View FTH Events.</span></span>

<span data-ttu-id="96348-121">Os eventos stop e Start do serviço não contêm dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="96348-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="96348-122">O evento habilitado para FTH contém a ID do processo (PID), o nome da imagem do processo e a hora de início da instância do processo.</span><span class="sxs-lookup"><span data-stu-id="96348-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="96348-123">**Desabilitando o heap tolerante a falhas**</span><span class="sxs-lookup"><span data-stu-id="96348-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="96348-124">**Cuidado** Problemas sérios podem ocorrer se você modificar o registro incorretamente usando o editor do registro ou usando outro método.</span><span class="sxs-lookup"><span data-stu-id="96348-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="96348-125">Esses problemas podem exigir a reinstalação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="96348-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="96348-126">A Microsoft não garante que esses problemas possam ser solucionados.</span><span class="sxs-lookup"><span data-stu-id="96348-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="96348-127">Modifique o Registro por conta própria.</span><span class="sxs-lookup"><span data-stu-id="96348-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="96348-128">Para desabilitar completamente o heap tolerante a falhas em um sistema, defina o valor do REG \_ DWORD como **HKLM \\ software \\ Microsoft \\ FTH \\ habilitado** como **0**.</span><span class="sxs-lookup"><span data-stu-id="96348-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="96348-129">Depois de alterar esse valor, reinicie o sistema.</span><span class="sxs-lookup"><span data-stu-id="96348-129">After changing this value, restart the system.</span></span> <span data-ttu-id="96348-130">O FTH não será mais ativado para novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="96348-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="96348-131">**Redefinindo a lista de aplicativos rastreados pelo FTH**</span><span class="sxs-lookup"><span data-stu-id="96348-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="96348-132">O heap tolerante a falhas é autogerenciável e interromperá a aplicação de forma autônoma, caso as atenuações não sejam efetivas para um determinado aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96348-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="96348-133">No entanto, se você precisar redefinir a lista de aplicativos para os quais o FTH está atenuando problemas (por exemplo, se você estiver testando um aplicativo e precisar reproduzir uma falha que o FTH está mitigando), poderá executar o seguinte comando em um prompt de comando elevado:  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="96348-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="96348-134">**Cuidado** A execução desse comando limpará todos os aplicativos FTH, para que os aplicativos que estão funcionando corretamente no momento possam começar a falhar novamente após a execução desse comando.</span><span class="sxs-lookup"><span data-stu-id="96348-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



