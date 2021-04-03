---
title: Descritor de segurança padrão
description: Com Active Directory Domain Services, você também pode especificar a segurança padrão para cada tipo de objeto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de descritor de segurança padrão
- descritores de segurança, AD, padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007333"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="01008-105">Descritor de segurança padrão</span><span class="sxs-lookup"><span data-stu-id="01008-105">Default Security Descriptor</span></span>

<span data-ttu-id="01008-106">Com Active Directory Domain Services, você também pode especificar a segurança padrão para cada tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="01008-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="01008-107">Isso é especificado no atributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) na definição do objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) no esquema de [Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="01008-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="01008-108">Esse descritor de segurança é usado para fornecer proteção padrão no objeto se não houver descritor de segurança especificado durante a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="01008-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="01008-109">As ACEs de um descritor de segurança padrão são manipuladas como se fossem especificadas como parte da criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="01008-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="01008-110">Portanto, as ACEs padrão são colocadas antes das ACEs herdadas e as substituem conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="01008-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="01008-111">Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="01008-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="01008-112">O [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) é especificado em um formato de cadeia de caracteres especial usando o SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).</span><span class="sxs-lookup"><span data-stu-id="01008-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="01008-113">Duas funções podem ser usadas para converter a forma binária do descritor de segurança para o formato de cadeia de caracteres e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="01008-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="01008-114">Essas funções são:</span><span class="sxs-lookup"><span data-stu-id="01008-114">These functions are:</span></span>

-   [<span data-ttu-id="01008-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="01008-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="01008-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="01008-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="01008-117">Para obter mais informações e os descritores de segurança padrão das classes de objeto predefinidas, consulte as páginas de referência de classe na referência de esquema de Active Directory da [referência de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="01008-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="01008-118">Para obter mais informações e um exemplo de código que lê ou modifica a propriedade [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de uma classe de objeto, consulte [lendo o DefaultSecurityDescriptor para uma classe de objeto](reading-the-defaultsecuritydescriptor-for-an-object-class.md) e [modificando o DefaultSecurityDescriptor para uma classe de objeto](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span><span class="sxs-lookup"><span data-stu-id="01008-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 