---
description: É o módulo do Windows que executa logon interativo para uma sessão de logon. O comportamento do Winlogon pode ser personalizado pela implementação e registro de um provedor de credenciais.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon e provedores de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920850"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="e4dba-104">Winlogon e provedores de credenciais</span><span class="sxs-lookup"><span data-stu-id="e4dba-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="e4dba-105">[*Winlogon*](../secgloss/w-gly.md) é o módulo do Windows que executa logon interativo para uma [*sessão de logon*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e4dba-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="e4dba-106">O comportamento do Winlogon pode ser personalizado pela implementação e registro de um provedor de credenciais.</span><span class="sxs-lookup"><span data-stu-id="e4dba-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="e4dba-107">Para obter informações sobre como implementar um provedor de credenciais, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4dba-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="e4dba-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="e4dba-108">Topic</span></span>                                                                                                           | <span data-ttu-id="e4dba-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4dba-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4dba-110">Experiência de logon do Windows controlada pelo provedor de credenciais</span><span class="sxs-lookup"><span data-stu-id="e4dba-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="e4dba-111">Visão geral do Winlogon e da arquitetura do provedor de credenciais e um provedor de credenciais de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e4dba-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="e4dba-112">Interfaces do Shell</span><span class="sxs-lookup"><span data-stu-id="e4dba-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="e4dba-113">Referência da interface do provedor de credenciais.</span><span class="sxs-lookup"><span data-stu-id="e4dba-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="e4dba-114">Provedores de credenciais no Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4dba-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="e4dba-115">Provedores de credenciais de terceiros e provedores de credenciais do sistema no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e4dba-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="e4dba-116">Para obter uma implementação de provedor de credenciais de exemplo, consulte o exemplo localizado no diretório de instalação SDK do Windows em \\ Samples \\ Security \\ credentialprovider.</span><span class="sxs-lookup"><span data-stu-id="e4dba-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="e4dba-117">**Windows Server 2003 e Windows XP:** Não há suporte para provedores de credenciais.</span><span class="sxs-lookup"><span data-stu-id="e4dba-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="e4dba-118">Para obter informações sobre como personalizar o Winlogon, consulte [Winlogon e Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="e4dba-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
