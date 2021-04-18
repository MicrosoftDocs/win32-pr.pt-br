---
description: A política de tíquete Kerberos é definida no nível de domínio e implementada pelo centro de distribuição de chaves do domínio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Política do Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752011"
---
# <a name="kerberos-policy"></a><span data-ttu-id="93fcb-103">Política do Kerberos</span><span class="sxs-lookup"><span data-stu-id="93fcb-103">Kerberos Policy</span></span>

<span data-ttu-id="93fcb-104">A política de tíquete Kerberos é definida no nível de domínio e implementada pelo [*centro de distribuição de chaves*](../secgloss/k-gly.md) do domínio (KDC).</span><span class="sxs-lookup"><span data-stu-id="93fcb-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="93fcb-105">A política Kerberos é armazenada no Active Directory como um subconjunto dos atributos da política de segurança de domínio.</span><span class="sxs-lookup"><span data-stu-id="93fcb-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="93fcb-106">Por padrão, as opções de política podem ser definidas somente por membros do grupo Administradores de domínio.</span><span class="sxs-lookup"><span data-stu-id="93fcb-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="93fcb-107">A diretiva de domínio inclui opções que:</span><span class="sxs-lookup"><span data-stu-id="93fcb-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="93fcb-108">Dar suporte a tíquetes pós-datados</span><span class="sxs-lookup"><span data-stu-id="93fcb-108">Support postdated tickets</span></span>
-   <span data-ttu-id="93fcb-109">Suporte à delegação restrita (somente Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="93fcb-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="93fcb-110">Tíquetes de suporte que podem ser encaminhados</span><span class="sxs-lookup"><span data-stu-id="93fcb-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="93fcb-111">Dar suporte a tíquetes renováveis</span><span class="sxs-lookup"><span data-stu-id="93fcb-111">Support renewable tickets</span></span>
-   <span data-ttu-id="93fcb-112">Definir idade máxima do tíquete</span><span class="sxs-lookup"><span data-stu-id="93fcb-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="93fcb-113">Definir idade de renovação máxima</span><span class="sxs-lookup"><span data-stu-id="93fcb-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="93fcb-114">Definir idade máxima do tíquete de proxy</span><span class="sxs-lookup"><span data-stu-id="93fcb-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="93fcb-115">Fazer logoff forçado dos usuários quando os tíquetes expiram</span><span class="sxs-lookup"><span data-stu-id="93fcb-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="93fcb-116">Com a [*delegação restrita*](../secgloss/c-gly.md), um computador pode ser definido para permitir o encaminhamento de credenciais somente para uma lista específica de serviços.</span><span class="sxs-lookup"><span data-stu-id="93fcb-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="93fcb-117">Esses serviços devem residir no mesmo domínio que o computador que encaminha as credenciais.</span><span class="sxs-lookup"><span data-stu-id="93fcb-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="93fcb-118">Sob a *delegação restrita*, os tíquetes não são mais enviados do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="93fcb-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="93fcb-119">O computador servidor cria tíquetes de serviço para encaminhar conforme necessário das informações usadas para autenticar o cliente.</span><span class="sxs-lookup"><span data-stu-id="93fcb-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="93fcb-120">Embora a diretiva Kerberos para um domínio possa permitir a autenticação delegada permitindo que os tíquetes sejam encaminhados, esse aspecto da diretiva não precisa se aplicar a todos os usuários ou a todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="93fcb-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="93fcb-121">Um atributo de uma conta de usuário individual pode ser definido para desabilitar o encaminhamento das [*credenciais*](../secgloss/c-gly.md) desse usuário por qualquer servidor.</span><span class="sxs-lookup"><span data-stu-id="93fcb-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="93fcb-122">Um atributo de uma conta de computador individual pode ser definido para desabilitar o encaminhamento de credenciais de qualquer usuário.</span><span class="sxs-lookup"><span data-stu-id="93fcb-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="93fcb-123">Em ambos os casos, a delegação pode ser desabilitada por meio da criação de uma política de grupo para ser aplicada a todos os usuários ou a todos os computadores em uma unidade organizacional do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93fcb-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="93fcb-124">**Windows XP/2000:** Não há suporte para a delegação restrita.</span><span class="sxs-lookup"><span data-stu-id="93fcb-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 
