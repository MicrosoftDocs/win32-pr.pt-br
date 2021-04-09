---
description: Os pais controlam as principais decisões de design
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Os pais controlam as principais decisões de design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011736"
---
# <a name="parental-controls-key-design-decisions"></a><span data-ttu-id="fb24a-103">Os pais controlam as principais decisões de design</span><span class="sxs-lookup"><span data-stu-id="fb24a-103">Parental Controls Key Design Decisions</span></span>

<span data-ttu-id="fb24a-104">As principais decisões de design no desenvolvimento de controles dos pais do Windows Vista são:</span><span class="sxs-lookup"><span data-stu-id="fb24a-104">Major design decisions in the development of Windows Vista Parental Controls are:</span></span>

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a><span data-ttu-id="fb24a-105">Dependência essencial no recurso UAC (controle de conta de usuário) do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb24a-105">Essential Dependency on Windows Vista User Account Control (UAC) Feature</span></span>

<span data-ttu-id="fb24a-106">Uma decisão importante para os controles dos pais do Windows Vista é contar com o novo recurso UAC (controle de conta de usuário) para implementar as identidades de conta de direitos reduzidas especialmente necessárias para restrições offline em usuários controlados.</span><span class="sxs-lookup"><span data-stu-id="fb24a-106">A key decision for Windows Vista Parental Controls is to rely on the new User Account Control (UAC) feature to implement the reduced rights account identities especially needed for offline restrictions on controlled users.</span></span> <span data-ttu-id="fb24a-107">Para obter mais informações sobre o UAC, consulte [a história do desenvolvedor do Windows Vista e do Windows Server 2008: requisitos de desenvolvimento de aplicativos do Windows Vista para UAC (controle de conta de usuário)](/previous-versions/aa905330(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="fb24a-107">For more information about UAC, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span></span> <span data-ttu-id="fb24a-108">Em resumo, cada conta com direitos de administrador efetivamente tem privilégios para executar a função pai ou de guardião de exibir dados de log e definir políticas.</span><span class="sxs-lookup"><span data-stu-id="fb24a-108">In summary, every account with administrator rights effectively has privileges to perform the parent or guardian role of viewing log data and setting policies.</span></span> <span data-ttu-id="fb24a-109">Os controles dos pais só podem ser definidos em usuários com direitos padrão (chamados anteriormente de contas de usuário com privilégios mínimos ou LUAs), pois apenas eles não podem alterar logs e configurações com ACLs (listas de controle de acesso) configuradas somente para os administradores gravarem.</span><span class="sxs-lookup"><span data-stu-id="fb24a-109">Parental controls may only be set on standard-rights users (formerly called Least-privileged User Accounts, or LUAs), as only they cannot alter logs and settings with Access Control Lists (ACLs) configured only for administrators to write.</span></span> <span data-ttu-id="fb24a-110">Em outras palavras:</span><span class="sxs-lookup"><span data-stu-id="fb24a-110">In other words:</span></span>

-   <span data-ttu-id="fb24a-111">Uma identidade pai ou guardião é implicitamente igual a uma conta que tem direitos de um administrador.</span><span class="sxs-lookup"><span data-stu-id="fb24a-111">A parent or guardian identity implicitly equals an account that has rights of an administrator.</span></span>
-   <span data-ttu-id="fb24a-112">Os usuários controlados de forma responsável devem ser usuários padrão.</span><span class="sxs-lookup"><span data-stu-id="fb24a-112">Parentally controlled users must be standard users.</span></span>

## <a name="nearly-all-settings-are-available-by-apis"></a><span data-ttu-id="fb24a-113">Quase todas as configurações estão disponíveis por APIs</span><span class="sxs-lookup"><span data-stu-id="fb24a-113">Nearly All Settings Are Available by APIs</span></span>

<span data-ttu-id="fb24a-114">Com exceção de itens como definições do sistema de classificação, as configurações disponíveis para manipulação pela interface do usuário de controles pais também podem ser modificadas por APIs expostas.</span><span class="sxs-lookup"><span data-stu-id="fb24a-114">With the exception of items such as ratings system definitions, settings available for manipulation by the Parental Controls User Interface may also be modified by exposed APIs.</span></span> <span data-ttu-id="fb24a-115">É necessário que os programas implementem a elevação a direitos administrativos a fim de alterar as configurações, conforme observado acima para o UAC.</span><span class="sxs-lookup"><span data-stu-id="fb24a-115">It is necessary for programs to implement elevation to administrative rights in order to alter settings, as noted above for UAC.</span></span>

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a><span data-ttu-id="fb24a-116">Os controles dos pais do Windows Vista são uma tecnologia somente para consumidores</span><span class="sxs-lookup"><span data-stu-id="fb24a-116">Windows Vista Parental Controls Is a Consumer-only Technology</span></span>

<span data-ttu-id="fb24a-117">Os controles dos pais do Windows Vista não se destinam a serem usados com contas de domínio.</span><span class="sxs-lookup"><span data-stu-id="fb24a-117">Windows Vista Parental Controls are not intended to be used with domain accounts.</span></span> <span data-ttu-id="fb24a-118">Como uma tecnologia de consumidor, os controles dos pais não são implantados em SKUs comerciais do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fb24a-118">As a consumer technology, Parental Controls is not deployed in business SKUs of Windows Vista.</span></span> <span data-ttu-id="fb24a-119">Se um computador tiver ingressado em um domínio, os links da interface do usuário de segurança da família serão suprimidos.</span><span class="sxs-lookup"><span data-stu-id="fb24a-119">If a computer is joined to a domain, the Family Safety user interface links will be suppressed.</span></span>

<span data-ttu-id="fb24a-120">Um mecanismo será fornecido para expor a funcionalidade para o caso ingressado no domínio, mas somente contas de usuário que não sejam de domínio poderão ser configuradas com controles dos pais.</span><span class="sxs-lookup"><span data-stu-id="fb24a-120">A mechanism will be provided to expose the functionality for the domain-joined case, but only non-domain user accounts may be configured with Parental Controls.</span></span>

 

 
