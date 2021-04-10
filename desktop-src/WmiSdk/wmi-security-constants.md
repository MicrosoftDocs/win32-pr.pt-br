---
description: O WMI verifica os direitos de acesso para aplicativos e scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de segurança do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171653"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="f2590-103">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="f2590-103">WMI Security Constants</span></span>

<span data-ttu-id="f2590-104">O WMI verifica os direitos de acesso de aplicativos e scripts para objetos como namespaces WMI, impressora, serviços, aplicativos DCOM, arquivos, compartilhamentos e outros objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="f2590-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="f2590-105">O acesso a esses objetos protegíveis é controlado pelas entradas de controle de acesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="f2590-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="f2590-106">Cada ACE contém listas que designam quais grupos ou usuários têm acesso.</span><span class="sxs-lookup"><span data-stu-id="f2590-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="f2590-107">Para obter mais informações sobre segurança e listas de controle de acesso (ACLs, DACLs ou SACLs), consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="f2590-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="f2590-108">Muitos métodos de provedor no WMI que afetam objetos protegíveis exigem que o administrador habilite determinados privilégios.</span><span class="sxs-lookup"><span data-stu-id="f2590-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="f2590-109">Qual versão do privilégio que você usa depende da linguagem de programação, conforme mostrado em [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f2590-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="f2590-110">As constantes de segurança são definidas nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f2590-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="f2590-111">**Constantes de segurança de evento**</span><span class="sxs-lookup"><span data-stu-id="f2590-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="f2590-112">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="f2590-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="f2590-113">**Constantes de direitos de acesso de namespace**</span><span class="sxs-lookup"><span data-stu-id="f2590-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="f2590-114">**Constantes do sinalizador ACE do namespace**</span><span class="sxs-lookup"><span data-stu-id="f2590-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="f2590-115">**Constantes de tipo de ACE de namespace**</span><span class="sxs-lookup"><span data-stu-id="f2590-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="f2590-116">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="f2590-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
