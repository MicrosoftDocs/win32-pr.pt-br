---
title: Requisitos do IIS para carregamentos do BITS
description: Para carregamentos, o BITS requer o IIS 6,0 no Windows Server 2003 e o IIS 7,0 no Windows Server 2008; O BITS não oferece suporte ao IIS 5,1 no Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635108"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="5db99-103">Requisitos do IIS para carregamentos do BITS</span><span class="sxs-lookup"><span data-stu-id="5db99-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="5db99-104">Para carregamentos, o BITS requer o IIS 6,0 no Windows Server 2003 e o IIS 7,0 no Windows Server 2008; O BITS não oferece suporte ao IIS 5,1 no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5db99-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="5db99-105">O diretório virtual do IIS deve ser habilitado para carregamentos e ter as extensões do IIS do BITS configuradas.</span><span class="sxs-lookup"><span data-stu-id="5db99-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="5db99-106">**Principais instalações do Windows Server:** Não há suporte para extensões do IIS do BITS.</span><span class="sxs-lookup"><span data-stu-id="5db99-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="5db99-107">No Windows Server 2008, use o **Gerenciador do servidor** para instalar o recurso de extensões de servidor bits.</span><span class="sxs-lookup"><span data-stu-id="5db99-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="5db99-108">Em **Gerenciador do servidor**, clique em **recursos** no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="5db99-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="5db99-109">No **Assistente para adicionar recursos**, marque extensões de servidor bits.</span><span class="sxs-lookup"><span data-stu-id="5db99-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="5db99-110">Observe que as funções de compatibilidade de gerenciamento do IIS 6 devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="5db99-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="5db99-111">No Windows Server 2003, use o **Assistente de componentes do Windows** para instalar a extensão do servidor bits.</span><span class="sxs-lookup"><span data-stu-id="5db99-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="5db99-112">No **painel de controle**, selecione **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="5db99-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="5db99-113">Em seguida, selecione **Adicionar/remover componentes do Windows** para exibir o **Assistente de componentes do Windows**.</span><span class="sxs-lookup"><span data-stu-id="5db99-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="5db99-114">A extensão do servidor BITS é um subcomponente do Serviços de Informações da Internet (IIS), que é um subcomponente do servidor de aplicativos da Web.</span><span class="sxs-lookup"><span data-stu-id="5db99-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="5db99-115">Se o serviço IISAdmin for reiniciado, o processo de trabalho do IIS deverá ser reciclado antes que o serviço BITS possa retomar os carregamentos.</span><span class="sxs-lookup"><span data-stu-id="5db99-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="5db99-116">O processo de trabalho do IIS pode ser reciclado manualmente usando o utilitário de linha de comando **IISReset.exe** .</span><span class="sxs-lookup"><span data-stu-id="5db99-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="5db99-117">Para obter informações sobre como configurar o IIS para carregamentos, consulte [Configurando o servidor para carregamentos](setting-up-the-server-for-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="5db99-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="5db99-118">Para obter detalhes sobre as propriedades que o BITS adiciona ao IIS, consulte [configurações do servidor bits para trabalhos de carregamento](bits-server-settings-for-upload-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="5db99-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 




