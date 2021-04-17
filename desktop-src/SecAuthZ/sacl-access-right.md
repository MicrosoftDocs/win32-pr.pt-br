---
description: O direito de acesso de segurança do sistema de acesso \_ \_ controla a capacidade de obter ou definir a SACL em um descritor de segurança de objetos. O sistema concede esse direito de acesso se o \_ privilégio nome de segurança se \_ estiver habilitado no token de acesso do thread solicitante.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Direito de acesso à SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754961"
---
# <a name="sacl-access-right"></a><span data-ttu-id="39f1d-104">Direito de acesso à SACL</span><span class="sxs-lookup"><span data-stu-id="39f1d-104">SACL Access Right</span></span>

<span data-ttu-id="39f1d-105">O direito de acesso de segurança do sistema de acesso \_ \_ controla a capacidade de obter ou definir a SACL no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto.</span><span class="sxs-lookup"><span data-stu-id="39f1d-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="39f1d-106">O sistema concede esse direito de acesso somente se o \_ privilégio nome de segurança se \_ estiver habilitado no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do thread solicitante.</span><span class="sxs-lookup"><span data-stu-id="39f1d-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="39f1d-107">**Para acessar a SACL de um objeto**</span><span class="sxs-lookup"><span data-stu-id="39f1d-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="39f1d-108">Chame a função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar o \_ privilégio de nome de segurança se \_ .</span><span class="sxs-lookup"><span data-stu-id="39f1d-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="39f1d-109">Solicite o \_ \_ direito acesso de segurança do sistema ao abrir um identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="39f1d-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="39f1d-110">Obtenha ou defina a SACL do objeto usando uma função como [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span><span class="sxs-lookup"><span data-stu-id="39f1d-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="39f1d-111">Chame [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para desabilitar o \_ privilégio nome de segurança se \_ .</span><span class="sxs-lookup"><span data-stu-id="39f1d-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="39f1d-112">Para acessar uma SACL usando as funções [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , habilite o \_ privilégio nome de segurança se \_ .</span><span class="sxs-lookup"><span data-stu-id="39f1d-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="39f1d-113">A função solicita o direito de acesso internamente.</span><span class="sxs-lookup"><span data-stu-id="39f1d-113">The function internally requests the access right.</span></span>

<span data-ttu-id="39f1d-114">O direito de acesso de segurança do sistema de acesso \_ \_ não é válido em uma DACL porque as DACLs não controlam o acesso a uma SACL.</span><span class="sxs-lookup"><span data-stu-id="39f1d-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="39f1d-115">No entanto, você pode usar o direito de acesso de segurança do sistema de acesso \_ \_ em uma SACL para auditar tentativas de usar o direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="39f1d-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
