---
title: Requisitos para funções de gerenciamento de rede em servidores e estações de trabalho
description: Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um servidor ou estação de trabalho, os requisitos de acesso diferentes se aplicarão a consultas de informações e atualizações de informações.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823941"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="d0056-103">Requisitos para funções de gerenciamento de rede em servidores e estações de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0056-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="d0056-104">Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um servidor ou estação de trabalho, os requisitos de acesso diferentes se aplicarão a consultas de informações e atualizações de informações.</span><span class="sxs-lookup"><span data-stu-id="d0056-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="d0056-105">Consultas</span><span class="sxs-lookup"><span data-stu-id="d0056-105">Queries</span></span>

<span data-ttu-id="d0056-106">Se você chamar uma das seguintes funções para executar uma consulta em um servidor ou estação de trabalho, por padrão, todos os usuários autenticados poderão ler e enumerar as informações.</span><span class="sxs-lookup"><span data-stu-id="d0056-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="d0056-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="d0056-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="d0056-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="d0056-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="d0056-109">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="d0056-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="d0056-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (somente níveis 1 e 2)</span><span class="sxs-lookup"><span data-stu-id="d0056-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="d0056-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (somente níveis 2 e 502)</span><span class="sxs-lookup"><span data-stu-id="d0056-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="d0056-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span><span class="sxs-lookup"><span data-stu-id="d0056-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="d0056-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="d0056-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="d0056-114">Veja a seguir informações adicionais sobre o acesso anônimo ao ler e enumerar informações.</span><span class="sxs-lookup"><span data-stu-id="d0056-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="d0056-115">**Windows Server 2003 e Windows XP:** O acesso anônimo a informações é possível se a configuração de política EveryoneIncludesAnonymous permitir acesso anônimo.</span><span class="sxs-lookup"><span data-stu-id="d0056-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="d0056-116">**Windows 2000:** O acesso anônimo a objetos protegíveis é possível se a configuração de política RestrictAnonymous permitir acesso anônimo.</span><span class="sxs-lookup"><span data-stu-id="d0056-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="d0056-117">Você pode restringir o acesso anônimo definindo a seguinte chave no registro para o valor 1.</span><span class="sxs-lookup"><span data-stu-id="d0056-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="d0056-118">**HKEY \_ \_Sistema de máquina local \\ \\ CurrentControlSet \\ controle \\ LSA** \\ **RestrictAnonymous** = 1</span><span class="sxs-lookup"><span data-stu-id="d0056-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="d0056-119">Para obter mais informações, consulte o seguinte artigo na base de dados de conhecimento Microsoft:</span><span class="sxs-lookup"><span data-stu-id="d0056-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="d0056-120">ID do artigo: [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="d0056-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="d0056-121">Título: como usar o valor do Registro RestrictAnonymous.</span><span class="sxs-lookup"><span data-stu-id="d0056-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="d0056-122">Atualizações</span><span class="sxs-lookup"><span data-stu-id="d0056-122">Updates</span></span>

<span data-ttu-id="d0056-123">Por padrão, somente administradores e usuários avançados podem gravar informações.</span><span class="sxs-lookup"><span data-stu-id="d0056-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="d0056-124">Para obter mais informações sobre como controlar o acesso a objetos protegíveis, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control), [privilégios](/windows/desktop/SecAuthZ/privileges)e [objetos protegíveis](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="d0056-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="d0056-125">Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="d0056-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 