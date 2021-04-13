---
description: Os termos a seguir descrevem os domínios que existem em sistemas remotos.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domínios primários e confiáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501544"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="4fddb-103">Domínios primários e confiáveis</span><span class="sxs-lookup"><span data-stu-id="4fddb-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="4fddb-104">Os termos a seguir descrevem os domínios que existem em sistemas remotos.</span><span class="sxs-lookup"><span data-stu-id="4fddb-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="4fddb-105">Domínio Primário</span><span class="sxs-lookup"><span data-stu-id="4fddb-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="4fddb-106">Domínio confiável</span><span class="sxs-lookup"><span data-stu-id="4fddb-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="4fddb-107">Domínio Primário</span><span class="sxs-lookup"><span data-stu-id="4fddb-107">Primary Domain</span></span>

<span data-ttu-id="4fddb-108">Um domínio primário é o domínio que é responsável por estabelecer relações de confiança adicionais e executar a autenticação (ou para passar uma solicitação de autenticação para um domínio confiável apropriado).</span><span class="sxs-lookup"><span data-stu-id="4fddb-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="4fddb-109">Os controladores de domínio no domínio primário tratam ou passam por solicitações de autenticação originadas na estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4fddb-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="4fddb-110">Quando ocorre o logon, a LSA verifica os domínios internos e de conta para obter informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4fddb-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="4fddb-111">Se a conta que está sendo conectada não estiver em nenhum desses domínios, a solicitação de logon será enviada para o domínio primário do sistema.</span><span class="sxs-lookup"><span data-stu-id="4fddb-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="4fddb-112">Domínio confiável</span><span class="sxs-lookup"><span data-stu-id="4fddb-112">Trusted Domain</span></span>

<span data-ttu-id="4fddb-113">Um domínio confiável é um domínio no qual o sistema local confia para autenticar usuários.</span><span class="sxs-lookup"><span data-stu-id="4fddb-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="4fddb-114">Em outras palavras, se um usuário ou aplicativo for autenticado por um domínio confiável, essa autenticação será aceita por todos os domínios que confiam no domínio de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4fddb-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="4fddb-115">Cada domínio subordinado tem automaticamente uma relação de confiança bidirecional com o domínio principal.</span><span class="sxs-lookup"><span data-stu-id="4fddb-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="4fddb-116">Por padrão, essa confiança é transitiva, o que significa que, se um sistema confiar no domínio A, ele também confiará em todos os domínios em que o domínio confia.</span><span class="sxs-lookup"><span data-stu-id="4fddb-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="4fddb-117">Também há suporte para relações de confiança unidirecionais em sistemas operacionais anteriores ao Windows 2000, que não dão suporte a relações de confiança bidirecionais transitivas.</span><span class="sxs-lookup"><span data-stu-id="4fddb-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="4fddb-118">A [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) tem um tipo de objeto, [**TrustedDomain**](the-trusteddomain-object-type.md), que é usado para armazenar informações sobre relações de confiança, incluindo o nome e o [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) (SID) do domínio confiável, a conta no domínio a ser usada para solicitações de autenticação, solicitações de conversão de nome e Sid e os nomes de controladores de domínio no domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="4fddb-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="4fddb-119">Em controladores de domínio, a LSA cria uma instância de um objeto [**TrustedDomain**](the-trusteddomain-object-type.md) para cada domínio confiável pelo sistema local.</span><span class="sxs-lookup"><span data-stu-id="4fddb-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="4fddb-120">Por exemplo, se uma estação de trabalho do Windows XP confiar em um controlador de domínio do Windows 2000 que, por sua vez, confiar em quatro outros sistemas, a estação de trabalho, conectada usando confiança transitiva, terá cinco objetos [**TrustedDomain**](the-trusteddomain-object-type.md) em seu sistema local.</span><span class="sxs-lookup"><span data-stu-id="4fddb-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 
