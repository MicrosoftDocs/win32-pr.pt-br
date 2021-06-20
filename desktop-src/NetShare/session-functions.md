---
description: Entenda as funções de sessão no gerenciamento de compartilhamento de rede. Essas funções controlam as sessões de rede estabelecidas entre estações de trabalho e servidores.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funções de sessão (gerenciamento de compartilhamento de rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409719"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="f926e-104">Funções de sessão (gerenciamento de compartilhamento de rede)</span><span class="sxs-lookup"><span data-stu-id="f926e-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="f926e-105">As funções de sessão de gerenciamento de rede controlam as sessões de rede estabelecidas entre estações de trabalho e servidores.</span><span class="sxs-lookup"><span data-stu-id="f926e-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="f926e-106">As funções exigem que o serviço do servidor seja iniciado no servidor.</span><span class="sxs-lookup"><span data-stu-id="f926e-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="f926e-107">As funções de sessão são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f926e-107">The session functions are listed following.</span></span>



| <span data-ttu-id="f926e-108">Função</span><span class="sxs-lookup"><span data-stu-id="f926e-108">Function</span></span>                                       | <span data-ttu-id="f926e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f926e-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f926e-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="f926e-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="f926e-111">Exclui as conexões atuais entre uma estação de trabalho e um servidor; encerra a sessão de rede.</span><span class="sxs-lookup"><span data-stu-id="f926e-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="f926e-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="f926e-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="f926e-113">Retorna informações sobre todas as sessões atuais estabelecidas para um servidor.</span><span class="sxs-lookup"><span data-stu-id="f926e-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="f926e-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f926e-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="f926e-115">Retorna informações sobre uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="f926e-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="f926e-116">Uma *sessão* é um link entre uma estação de trabalho e um servidor.</span><span class="sxs-lookup"><span data-stu-id="f926e-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="f926e-117">Uma sessão é estabelecida na primeira vez em que uma estação de trabalho faz uma conexão com um recurso compartilhado no servidor.</span><span class="sxs-lookup"><span data-stu-id="f926e-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="f926e-118">Até que a sessão termine, todas as conexões adicionais entre a estação de trabalho e o servidor fazem parte da mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="f926e-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="f926e-119">Para encerrar uma sessão, um aplicativo na extremidade do servidor de uma conexão chama a função [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .</span><span class="sxs-lookup"><span data-stu-id="f926e-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="f926e-120">As funções de sessão de gerenciamento de rede gerenciam informações em uma base por usuário com o parâmetro *username* .</span><span class="sxs-lookup"><span data-stu-id="f926e-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="f926e-121">Como pode haver vários usuários por sessão, esse parâmetro é necessário para acessar as informações específicas do usuário para a sessão.</span><span class="sxs-lookup"><span data-stu-id="f926e-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="f926e-122">As funções de sessão estão disponíveis em cinco níveis de informações:</span><span class="sxs-lookup"><span data-stu-id="f926e-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="f926e-123">**Informações da sessão \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="f926e-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="f926e-124">**Informações da sessão \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f926e-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="f926e-125">**Informações da sessão \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f926e-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="f926e-126">**Informações da sessão \_ \_ 10**</span><span class="sxs-lookup"><span data-stu-id="f926e-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="f926e-127">**Informações da sessão \_ \_ 502**</span><span class="sxs-lookup"><span data-stu-id="f926e-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="f926e-128">Se você estiver programando para Active Directory, poderá chamar determinados métodos da interface de serviço Active Directory (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções de sessão de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="f926e-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="f926e-129">Para obter mais informações, consulte [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="f926e-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
