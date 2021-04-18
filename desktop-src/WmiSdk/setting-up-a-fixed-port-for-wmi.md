---
description: O WMI é executado como parte de um host de serviço compartilhado com portas atribuídas por meio de DCOM por padrão. No entanto, você pode configurar o serviço WMI para ser executado como o único processo em um host separado e especificar uma porta fixa.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configurando uma porta fixa para o WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807959"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="bb8c1-104">Configurando uma porta fixa para o WMI</span><span class="sxs-lookup"><span data-stu-id="bb8c1-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="bb8c1-105">O WMI é executado como parte de um host de serviço compartilhado com portas atribuídas por meio de DCOM por padrão.</span><span class="sxs-lookup"><span data-stu-id="bb8c1-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="bb8c1-106">No entanto, você pode configurar o serviço WMI para ser executado como o único processo em um host separado e especificar uma porta fixa.</span><span class="sxs-lookup"><span data-stu-id="bb8c1-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="bb8c1-107">O procedimento a seguir é uma configuração automatizada para permitir que o WMI tenha uma porta fixa.</span><span class="sxs-lookup"><span data-stu-id="bb8c1-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="bb8c1-108">O procedimento usa a ferramenta de linha de comando [**winmgmt**](winmgmt.md) .</span><span class="sxs-lookup"><span data-stu-id="bb8c1-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="bb8c1-109">**Para configurar uma porta fixa para o WMI**</span><span class="sxs-lookup"><span data-stu-id="bb8c1-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="bb8c1-110">No prompt de comando, digite **winmgmt-standalonehost**</span><span class="sxs-lookup"><span data-stu-id="bb8c1-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="bb8c1-111">Pare o serviço WMI digitando o comando **net stop "Instrumentação de gerenciamento do Windows"** ou use o nome curto de **winmgmt do net stop**</span><span class="sxs-lookup"><span data-stu-id="bb8c1-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="bb8c1-112">Reinicie o serviço WMI novamente em um novo host de serviço digitando **net start "Instrumentação de gerenciamento do Windows"** ou **net start winmgmt**</span><span class="sxs-lookup"><span data-stu-id="bb8c1-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="bb8c1-113">Estabeleça um novo número de porta para o serviço WMI digitando **netsh firewall add abertura TCP 24158 WMIFixedPort**</span><span class="sxs-lookup"><span data-stu-id="bb8c1-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="bb8c1-114">Para desfazer as alterações feitas no WMI, digite **winmgmt/sharedhost** e, em seguida, pare e inicie o serviço Winmgmt novamente.</span><span class="sxs-lookup"><span data-stu-id="bb8c1-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="bb8c1-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb8c1-115">Examples</span></span>

<span data-ttu-id="bb8c1-116">Para obter um script que configura uma porta fixa para o WMI, consulte o [exemplo de código](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )da Galeria de scripts a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb8c1-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="bb8c1-117">ou um exemplo de código do PowerShell que habilita ou desabilita as configurações de porta WMI, consulte o exemplo [set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) na galeria do TechNet.</span><span class="sxs-lookup"><span data-stu-id="bb8c1-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb8c1-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb8c1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8c1-119">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="bb8c1-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="bb8c1-120">Solucionando problemas de conexões WMI remotas</span><span class="sxs-lookup"><span data-stu-id="bb8c1-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="bb8c1-121">Hospedagem e segurança de provedor</span><span class="sxs-lookup"><span data-stu-id="bb8c1-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



