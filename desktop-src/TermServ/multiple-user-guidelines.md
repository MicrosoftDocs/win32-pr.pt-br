---
title: Diretrizes de vários usuários
description: Diretrizes para o desenvolvimento de aplicativos para vários usuários em um ambiente de Serviços de Área de Trabalho Remota.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788032"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="c1af3-103">Diretrizes de vários usuários</span><span class="sxs-lookup"><span data-stu-id="c1af3-103">Multiple-user guidelines</span></span>

<span data-ttu-id="c1af3-104">As seções a seguir fornecem diretrizes para o desenvolvimento de aplicativos para vários usuários em um ambiente de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="c1af3-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1af3-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c1af3-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c1af3-106">Instalação do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1af3-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="c1af3-107">A instalação de um aplicativo para um único usuário pode criar problemas em um ambiente de Serviços de Área de Trabalho Remota multiusuário.</span><span class="sxs-lookup"><span data-stu-id="c1af3-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="c1af3-108">Armazenando informações específicas do usuário</span><span class="sxs-lookup"><span data-stu-id="c1af3-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="c1af3-109">Aplicativos devem armazenar informações específicas do usuário em locais específicos do usuário, separadamente de informações globais que se aplicam a todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="c1af3-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="c1af3-110">Namespaces de objeto kernel</span><span class="sxs-lookup"><span data-stu-id="c1af3-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="c1af3-111">Serviços de Área de Trabalho Remota usa vários namespaces para objetos kernel; um namespace global é usado principalmente por serviços em aplicativos cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="c1af3-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="c1af3-112">Endereços IP e nomes de computador</span><span class="sxs-lookup"><span data-stu-id="c1af3-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="c1af3-113">Não é seguro pressupor que o nome do computador ou o endereço IP atribuído ao computador está associados um único usuário, pois vários usuários podem ser conectados simultaneamente a um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="c1af3-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="c1af3-114">Como sempre, bloqueie arquivos e bancos de dados ao fazer alterações para evitar a perda inadvertida de dado.</span><span class="sxs-lookup"><span data-stu-id="c1af3-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="c1af3-115">Seu aplicativo não deve bloquear nenhum arquivo de aplicativo em tempo de execução que não seja de arquivos por usuário.</span><span class="sxs-lookup"><span data-stu-id="c1af3-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="c1af3-116">Arquivos de tempo de execução bloqueados podem manter várias instâncias do aplicativo ou os processos sob o aplicativo, como assistentes, de serem executados.</span><span class="sxs-lookup"><span data-stu-id="c1af3-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="c1af3-117">Uma boa maneira de testar quais arquivos são arquivos de aplicativo em tempo de execução é controlar quais arquivos são instalados pela instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1af3-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="c1af3-118">Arquivos por usuário raramente são instalados pela instalação; Portanto, a maioria dos arquivos instalados pela instalação são arquivos de aplicativo de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c1af3-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




