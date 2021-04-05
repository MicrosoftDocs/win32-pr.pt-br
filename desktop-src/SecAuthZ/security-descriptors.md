---
description: Um descritor de segurança contém as informações de segurança associadas a um objeto protegível.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descritores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827333"
---
# <a name="security-descriptors"></a><span data-ttu-id="74147-103">Descritores de segurança</span><span class="sxs-lookup"><span data-stu-id="74147-103">Security Descriptors</span></span>

<span data-ttu-id="74147-104">Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) contém as informações de segurança associadas a um [objeto protegível](securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="74147-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="74147-105">Um descritor de segurança consiste em uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e suas informações de segurança associadas.</span><span class="sxs-lookup"><span data-stu-id="74147-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="74147-106">Um descritor de segurança pode incluir as seguintes informações de segurança:</span><span class="sxs-lookup"><span data-stu-id="74147-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="74147-107">[Identificadores de segurança](security-identifiers.md) (SIDs) para o proprietário e o grupo primário de um objeto.</span><span class="sxs-lookup"><span data-stu-id="74147-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="74147-108">Uma [DACL](access-control-lists.md) que especifica os direitos de acesso permitidos ou negados a usuários ou grupos específicos.</span><span class="sxs-lookup"><span data-stu-id="74147-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="74147-109">Uma [SACL](access-control-lists.md) que especifica os tipos de tentativas de acesso que geram registros de auditoria para o objeto.</span><span class="sxs-lookup"><span data-stu-id="74147-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="74147-110">Um conjunto de bits de controle que qualifica o significado de um descritor de segurança ou seus membros individuais.</span><span class="sxs-lookup"><span data-stu-id="74147-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="74147-111">Os aplicativos não devem manipular diretamente o conteúdo de um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="74147-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="74147-112">A API do Windows fornece funções para configurar e recuperar as informações de segurança no descritor de segurança de um objeto.</span><span class="sxs-lookup"><span data-stu-id="74147-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="74147-113">Além disso, há funções para criar e inicializar um descritor de segurança para um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="74147-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="74147-114">Os aplicativos que trabalham com descritores de segurança em Active Directory objetos podem usar as funções de segurança do Windows ou as interfaces de segurança fornecidas pelas interfaces de serviço do Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="74147-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="74147-115">Para obter mais informações sobre as interfaces de segurança ADSI, consulte [como o controle de acesso funciona no Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="74147-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 
