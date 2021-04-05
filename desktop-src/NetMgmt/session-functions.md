---
title: Funções de sessão (gerenciamento de rede)
description: As funções de sessão de gerenciamento de rede controlam as sessões de rede estabelecidas entre estações de trabalho e servidores. As funções exigem que o serviço do servidor seja iniciado no servidor.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824118"
---
# <a name="session-functions-network-management"></a><span data-ttu-id="0058f-104">Funções de sessão (gerenciamento de rede)</span><span class="sxs-lookup"><span data-stu-id="0058f-104">Session Functions (Network Management)</span></span>

<span data-ttu-id="0058f-105">As funções de sessão de gerenciamento de rede controlam as sessões de rede estabelecidas entre estações de trabalho e servidores.</span><span class="sxs-lookup"><span data-stu-id="0058f-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="0058f-106">As funções exigem que o serviço do servidor seja iniciado no servidor.</span><span class="sxs-lookup"><span data-stu-id="0058f-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="0058f-107">As funções de sessão são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0058f-107">The session functions are listed following.</span></span>



| <span data-ttu-id="0058f-108">Função</span><span class="sxs-lookup"><span data-stu-id="0058f-108">Function</span></span>                                      | <span data-ttu-id="0058f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0058f-109">Description</span></span>                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0058f-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="0058f-110">**NetSessionDel**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="0058f-111">Exclui as conexões atuais entre uma estação de trabalho e um servidor; encerra a sessão de rede.</span><span class="sxs-lookup"><span data-stu-id="0058f-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="0058f-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="0058f-112">**NetSessionEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="0058f-113">Retorna informações sobre todas as sessões atuais estabelecidas para um servidor.</span><span class="sxs-lookup"><span data-stu-id="0058f-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="0058f-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0058f-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="0058f-115">Retorna informações sobre uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="0058f-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="0058f-116">Uma *sessão* é um link entre uma estação de trabalho e um servidor.</span><span class="sxs-lookup"><span data-stu-id="0058f-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="0058f-117">Uma sessão é estabelecida na primeira vez em que uma estação de trabalho faz uma conexão com um recurso compartilhado no servidor.</span><span class="sxs-lookup"><span data-stu-id="0058f-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="0058f-118">Até que a sessão termine, todas as conexões adicionais entre a estação de trabalho e o servidor fazem parte da mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="0058f-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="0058f-119">Para encerrar uma sessão, um aplicativo na extremidade do servidor de uma conexão chama a função [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) .</span><span class="sxs-lookup"><span data-stu-id="0058f-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="0058f-120">As funções de sessão de gerenciamento de rede gerenciam informações em uma base por usuário com o parâmetro *username* .</span><span class="sxs-lookup"><span data-stu-id="0058f-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="0058f-121">Como pode haver vários usuários por sessão, esse parâmetro é necessário para acessar as informações específicas do usuário para a sessão.</span><span class="sxs-lookup"><span data-stu-id="0058f-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="0058f-122">As funções de sessão estão disponíveis nos seguintes níveis de informações:</span><span class="sxs-lookup"><span data-stu-id="0058f-122">Session functions are available at the following information levels:</span></span>

-   [<span data-ttu-id="0058f-123">**Informações da sessão \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="0058f-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [<span data-ttu-id="0058f-124">**Informações da sessão \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0058f-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [<span data-ttu-id="0058f-125">**Informações da sessão \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0058f-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [<span data-ttu-id="0058f-126">**Informações da sessão \_ \_ 10**</span><span class="sxs-lookup"><span data-stu-id="0058f-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [<span data-ttu-id="0058f-127">**Informações da sessão \_ \_ 502**</span><span class="sxs-lookup"><span data-stu-id="0058f-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

<span data-ttu-id="0058f-128">Se você estiver programando para Active Directory, poderá chamar determinados métodos da interface de serviço Active Directory (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções de sessão de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="0058f-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="0058f-129">Para obter mais informações, consulte [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="0058f-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
