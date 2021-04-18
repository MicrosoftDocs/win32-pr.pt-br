---
title: Funções de usuário da estação de trabalho e estação de trabalho
description: As funções de estação de trabalho de gerenciamento de rede executam tarefas administrativas em uma estação de trabalho local ou remota.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811825"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="df3bb-103">Funções de usuário da estação de trabalho e estação de trabalho</span><span class="sxs-lookup"><span data-stu-id="df3bb-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="df3bb-104">As funções de estação de trabalho de gerenciamento de rede executam tarefas administrativas em uma estação de trabalho local ou remota.</span><span class="sxs-lookup"><span data-stu-id="df3bb-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="df3bb-105">Somente um usuário ou aplicativo com associação de grupo de administradores, em um servidor local ou remoto, pode executar tarefas administrativas em uma estação de trabalho para controlar sua operação, acesso do usuário e compartilhamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="df3bb-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="df3bb-106">Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="df3bb-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="df3bb-107">As funções de estação de trabalho são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="df3bb-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="df3bb-108">Função</span><span class="sxs-lookup"><span data-stu-id="df3bb-108">Function</span></span>                                   | <span data-ttu-id="df3bb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="df3bb-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="df3bb-110">**NetWkstaGetInfo**</span><span class="sxs-lookup"><span data-stu-id="df3bb-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="df3bb-111">Retorna informações sobre os elementos de configuração para uma estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="df3bb-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="df3bb-112">**NetWkstaSetInfo**</span><span class="sxs-lookup"><span data-stu-id="df3bb-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="df3bb-113">Configura uma estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="df3bb-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="df3bb-114">As funções de estação de trabalho permitem o acesso a dois tipos discretos de informações de estação de trabalho:</span><span class="sxs-lookup"><span data-stu-id="df3bb-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="df3bb-115">Informações do sistema</span><span class="sxs-lookup"><span data-stu-id="df3bb-115">System information</span></span>
-   <span data-ttu-id="df3bb-116">Informações específicas da plataforma</span><span class="sxs-lookup"><span data-stu-id="df3bb-116">Platform-specific information</span></span>

<span data-ttu-id="df3bb-117">Dentro de cada tipo, os dados são categorizados pelo acesso de segurança.</span><span class="sxs-lookup"><span data-stu-id="df3bb-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="df3bb-118">Os dados acessíveis ao convidado são um subconjunto dos dados acessíveis pelo usuário, que, por sua vez, são um subconjunto dos dados acessíveis ao administrador.</span><span class="sxs-lookup"><span data-stu-id="df3bb-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="df3bb-119">As informações da estação de trabalho estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="df3bb-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="df3bb-120">**Informações de WKSTA \_ \_ 100**</span><span class="sxs-lookup"><span data-stu-id="df3bb-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="df3bb-121">**Informações de WKSTA \_ \_ 101**</span><span class="sxs-lookup"><span data-stu-id="df3bb-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="df3bb-122">**Informações de WKSTA \_ \_ 102**</span><span class="sxs-lookup"><span data-stu-id="df3bb-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="df3bb-123">As funções de usuário da estação de trabalho de gerenciamento de rede permitem acesso a informações específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="df3bb-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="df3bb-124">As informações específicas do usuário são separadas das informações da estação de trabalho porque pode haver mais de um usuário em uma estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="df3bb-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="df3bb-125">As funções de usuário da estação de trabalho são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="df3bb-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="df3bb-126">Função</span><span class="sxs-lookup"><span data-stu-id="df3bb-126">Function</span></span>                                           | <span data-ttu-id="df3bb-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="df3bb-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="df3bb-128">**NetWkstaUserEnum**</span><span class="sxs-lookup"><span data-stu-id="df3bb-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="df3bb-129">Lista informações sobre todos os usuários conectados no momento à estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="df3bb-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="df3bb-130">**NetWkstaUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="df3bb-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="df3bb-131">Retorna informações sobre um usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="df3bb-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="df3bb-132">**NetWkstaUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="df3bb-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="df3bb-133">Define as informações específicas do usuário para os elementos de configuração de uma estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="df3bb-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="df3bb-134">As informações de usuário da estação de trabalho estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="df3bb-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="df3bb-135">**Informações do usuário do WKSTA \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="df3bb-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="df3bb-136">**Informações de usuário do WKSTA \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="df3bb-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="df3bb-137">**Informações do usuário do WKSTA \_ \_ \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="df3bb-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 