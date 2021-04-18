---
description: A partir do Windows Server 2008, o provedor de recursos do servidor fornece informações sobre quais recursos de servidor estão instalados no servidor. Essa classe permite que os administradores inventariam e gerenciem suas funções e recursos de servidor.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Provedor de recursos do servidor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807907"
---
# <a name="server-feature-provider"></a><span data-ttu-id="4cb1e-104">Provedor de recursos do servidor</span><span class="sxs-lookup"><span data-stu-id="4cb1e-104">Server Feature Provider</span></span>

<span data-ttu-id="4cb1e-105">A partir do Windows Server 2008, o provedor de recursos do servidor fornece informações sobre quais recursos de servidor estão instalados no servidor.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="4cb1e-106">Essa classe permite que os administradores inventariam e gerenciem suas funções e recursos de servidor.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="4cb1e-107">Uma função de servidor é definida como um grupo de componentes que fornecem funções para uma área específica de funcionalidade, como impressão, arquivos, controle de domínio e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="4cb1e-108">As funções de servidor típicas são servidor de arquivos, servidor de email, servidor DNS, controlador de domínio, servidor de aplicativos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="4cb1e-109">Se uma empresa não estiver executando um software de gerenciamento que relate funções de servidor, como o Microsoft Operations Manager com pacotes de gerenciamento instalados, você poderá obter essas informações consultando a classe [**Win32 \_ ServerFeature**](win32-serverfeature.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb1e-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="4cb1e-110">As informações de função e recurso de servidor de computadores remotos estão disponíveis por meio de conexões remotas WMI normais ou usando o Serviço Gerenciamento Remoto do Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="4cb1e-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="4cb1e-111">Para obter mais informações sobre conexões DCOM remotas do WMI, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4cb1e-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="4cb1e-112">Para obter mais informações sobre conexões usando o protocolo [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , consulte [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal).</span><span class="sxs-lookup"><span data-stu-id="4cb1e-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="4cb1e-113">O provedor de recursos do servidor dá suporte às seguintes classes WMI:</span><span class="sxs-lookup"><span data-stu-id="4cb1e-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="4cb1e-114">**\_ServerFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="4cb1e-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="4cb1e-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cb1e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cb1e-116">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="4cb1e-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
