---
description: Explica a linguagem de definição do descritor de segurança (SDDL).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Linguagem de definição do descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827336"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="8a1ac-103">Linguagem de definição do descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="8a1ac-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="8a1ac-104">O SDDL (Security Descriptor Definition Language) define o formato de cadeia de caracteres que as funções [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usam para descrever um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="8a1ac-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="8a1ac-105">O idioma também define elementos de cadeia de caracteres para descrever informações nos componentes de um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="8a1ac-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="8a1ac-106">As ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) condicional) têm um formato SDDL diferente dos outros tipos ACE.</span><span class="sxs-lookup"><span data-stu-id="8a1ac-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="8a1ac-107">Para ACEs, consulte [seqüências de caracteres Ace](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="8a1ac-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="8a1ac-108">Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="8a1ac-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a1ac-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a1ac-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a1ac-110">Formato de cadeia de caracteres descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="8a1ac-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="8a1ac-111">Linguagem de definição do descritor de segurança para ACEs condicionais</span><span class="sxs-lookup"><span data-stu-id="8a1ac-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="8a1ac-112">Cadeias de caracteres ACE</span><span class="sxs-lookup"><span data-stu-id="8a1ac-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="8a1ac-113">Cadeias de caracteres de SID</span><span class="sxs-lookup"><span data-stu-id="8a1ac-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="8a1ac-114">[\[MS-DTYP \] : linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="8a1ac-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
