---
title: Iniciando e parando o Microsoft Locator
description: As bibliotecas de tempo de execução RPC iniciam automaticamente o Microsoft Locator quando necessário. Você pode parar e iniciar o localizador manualmente se, por exemplo, precisar limpar o banco de dados durante a depuração de um aplicativo distribuído.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004803"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="f75c6-104">Iniciando e parando o Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="f75c6-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="f75c6-105">As bibliotecas de tempo de execução RPC iniciam automaticamente o Microsoft Locator quando necessário.</span><span class="sxs-lookup"><span data-stu-id="f75c6-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="f75c6-106">Você pode parar e iniciar o localizador manualmente se, por exemplo, precisar limpar o banco de dados durante a depuração de um aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="f75c6-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="f75c6-107">**Para parar e iniciar o Microsoft Locator**</span><span class="sxs-lookup"><span data-stu-id="f75c6-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="f75c6-108">No painel de controle, clique no ícone serviços.</span><span class="sxs-lookup"><span data-stu-id="f75c6-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="f75c6-109">A caixa de diálogo **Serviços** é exibida.</span><span class="sxs-lookup"><span data-stu-id="f75c6-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="f75c6-110">Na caixa de diálogo **serviço** , selecione **Microsoft Locator** e, em seguida, clique em **Iniciar** ou **parar**.</span><span class="sxs-lookup"><span data-stu-id="f75c6-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="f75c6-111">Você também pode iniciar e parar o localizador da Microsoft na linha de comando digitando:</span><span class="sxs-lookup"><span data-stu-id="f75c6-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="f75c6-112">**NET \[ Start/Stop \] RpcLocator**</span><span class="sxs-lookup"><span data-stu-id="f75c6-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="f75c6-113">Somente um administrador pode iniciar o Microsoft Locator quando ele for interrompido.</span><span class="sxs-lookup"><span data-stu-id="f75c6-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="f75c6-114">Se for interrompido, ele será reiniciado conforme necessário pelas bibliotecas de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="f75c6-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




