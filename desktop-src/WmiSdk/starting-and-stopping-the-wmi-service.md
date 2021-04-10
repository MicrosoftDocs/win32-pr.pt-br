---
description: O WMI é executado como um serviço com o nome de exibição &\# 0034; Instrumentação de Gerenciamento do Windows&\# 0034; e o nome do serviço &\# 0034; winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Iniciando e parando o serviço WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165202"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="17929-103">Iniciando e parando o serviço WMI</span><span class="sxs-lookup"><span data-stu-id="17929-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="17929-104">O WMI é executado como um serviço com o nome de exibição "Instrumentação de Gerenciamento do Windows" e o nome do serviço "winmgmt".</span><span class="sxs-lookup"><span data-stu-id="17929-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="17929-105">O WMI é executado automaticamente na inicialização do sistema na conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="17929-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="17929-106">Se o WMI não estiver em execução, ele será iniciado automaticamente quando o primeiro aplicativo de gerenciamento ou script solicitar conexão a um namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="17929-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="17929-107">Vários outros serviços dependem do serviço WMI, dependendo da versão do sistema operacional que o sistema está executando.</span><span class="sxs-lookup"><span data-stu-id="17929-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="17929-108">Iniciando o serviço Winmgmt</span><span class="sxs-lookup"><span data-stu-id="17929-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="17929-109">O procedimento a seguir descreve como iniciar o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="17929-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="17929-110">**Para iniciar o serviço Winmgmt**</span><span class="sxs-lookup"><span data-stu-id="17929-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="17929-111">Em um prompt de comando, digite **net** **Start** **winmgmt** \[ */<switch>* \] .</span><span class="sxs-lookup"><span data-stu-id="17929-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="17929-112">Para obter mais informações sobre as opções disponíveis, consulte [winmgmt](winmgmt.md).</span><span class="sxs-lookup"><span data-stu-id="17929-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="17929-113">Você usa a conta de administrador interna ou uma conta no grupo Administradores executando com direitos elevados para iniciar o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="17929-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="17929-114">Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="17929-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="17929-115">Outros serviços que dependem do serviço WMI, como o host de agente do SMS ou o Firewall do Windows, não serão reiniciados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="17929-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="17929-116">Parando o serviço Winmgmt</span><span class="sxs-lookup"><span data-stu-id="17929-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="17929-117">O procedimento a seguir descreve como interromper o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="17929-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="17929-118">**Para interromper o serviço Winmgmt**</span><span class="sxs-lookup"><span data-stu-id="17929-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="17929-119">Em um prompt de comando, digite **net stop winmgmt**.</span><span class="sxs-lookup"><span data-stu-id="17929-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="17929-120">Outros serviços que dependem do serviço WMI também são interrompidos, como o host de agente do SMS ou o Firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="17929-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="17929-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17929-121">Examples</span></span>

<span data-ttu-id="17929-122">A galeria do TechNet contém o [script Watchdog do serviço WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), que descreve como desligar e reiniciar programaticamente o serviço Winmgmt com o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="17929-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17929-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17929-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17929-124">Usando as ferramentas de Command-Line do WMI</span><span class="sxs-lookup"><span data-stu-id="17929-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



