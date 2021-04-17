---
title: Sobre a administração do serviço de acesso remoto
description: O Windows 2000 e sistemas operacionais posteriores fornecem um conjunto de funções para administrar permissões e portas de usuário em servidores RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Serviço de roteamento e acesso remoto RRAS, administração de RAS
- Serviço de roteamento e acesso remoto RRAS, administração de RAS, descrito
- RRAS de administração RAS
- Administração de RAS RRAS, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759604"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="d36f3-107">Sobre a administração do serviço de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="d36f3-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="d36f3-108">O Windows 2000 e sistemas operacionais posteriores fornecem um conjunto de funções para administrar permissões e portas de usuário em servidores RAS.</span><span class="sxs-lookup"><span data-stu-id="d36f3-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="d36f3-109">Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="d36f3-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="d36f3-110">Enumerar os usuários que têm um conjunto especificado de permissões de RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="d36f3-111">Atribuir ou revogar permissões RAS para um usuário especificado</span><span class="sxs-lookup"><span data-stu-id="d36f3-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="d36f3-112">Enumerar as portas configuradas em um servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="d36f3-113">Obter informações e estatísticas sobre uma porta especificada em um servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="d36f3-114">Redefinir os contadores de estatísticas para uma porta especificada</span><span class="sxs-lookup"><span data-stu-id="d36f3-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="d36f3-115">Desconectar uma porta especificada</span><span class="sxs-lookup"><span data-stu-id="d36f3-115">Disconnect a specified port</span></span>

<span data-ttu-id="d36f3-116">Você também pode instalar uma DLL de administração do servidor RAS para auditar conexões de usuário e atribuir endereços IP a usuários de discagem.</span><span class="sxs-lookup"><span data-stu-id="d36f3-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="d36f3-117">A DLL exporta um conjunto de funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.</span><span class="sxs-lookup"><span data-stu-id="d36f3-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="d36f3-118">Esta documentação descreve os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d36f3-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="d36f3-119">Comparação de funções: Windows 2000 x RRAS redistribuível</span><span class="sxs-lookup"><span data-stu-id="d36f3-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="d36f3-120">Administração de usuário RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="d36f3-121">Administração de porta e servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="d36f3-122">DLL de administração de RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="d36f3-123">Configuração do registro da DLL de administração do RAS</span><span class="sxs-lookup"><span data-stu-id="d36f3-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 




