---
description: O formato de cadeia de caracteres do descritor de segurança é um formato de texto para armazenar ou transportar informações em um descritor de segurança.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Formato de cadeia de caracteres descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7fd6e9e2387deee63b5046086ed167a29fa54b
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644198"
---
# <a name="security-descriptor-string-format"></a><span data-ttu-id="5491e-103">Formato de cadeia de caracteres descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="5491e-103">Security Descriptor String Format</span></span>

<span data-ttu-id="5491e-104">O **formato de cadeia de caracteres do descritor de segurança** é um formato de texto para armazenar ou transportar informações em um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="5491e-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="5491e-105">As funções [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usam esse formato.</span><span class="sxs-lookup"><span data-stu-id="5491e-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="5491e-106">O formato é uma cadeia de caracteres terminada em **nulo** com tokens para indicar cada um dos quatro componentes principais de um descritor de segurança: proprietário (O:), grupo primário (G:), DACL (D:) e SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="5491e-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="5491e-107">[*As*](/windows/desktop/SecGloss/a-gly) ACEs (entradas de controle de acesso) e as ACEs condicionais têm formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="5491e-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="5491e-108">Para ACEs, consulte [seqüências de caracteres Ace](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5491e-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="5491e-109">Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="5491e-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="5491e-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>Sid do proprietário \_</span><span class="sxs-lookup"><span data-stu-id="5491e-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="5491e-111">Uma [cadeia de caracteres Sid](sid-strings.md) que identifica o proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="5491e-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="5491e-112"><span id="group_sid"></span><span id="GROUP_SID"></span>Sid do grupo \_</span><span class="sxs-lookup"><span data-stu-id="5491e-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="5491e-113">Uma cadeia de caracteres SID que identifica o grupo primário do objeto.</span><span class="sxs-lookup"><span data-stu-id="5491e-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="5491e-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>sinalizadores de DACL \_</span><span class="sxs-lookup"><span data-stu-id="5491e-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="5491e-115">Sinalizadores de controle do descritor de segurança que se aplicam à DACL.</span><span class="sxs-lookup"><span data-stu-id="5491e-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="5491e-116">Para obter uma descrição desses sinalizadores de controle, consulte a função [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .</span><span class="sxs-lookup"><span data-stu-id="5491e-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="5491e-117">A \_ cadeia de caracteres de sinalizadores DACL pode ser uma concatenação de zero ou mais das cadeias de caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="5491e-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="5491e-118">Control</span><span class="sxs-lookup"><span data-stu-id="5491e-118">Control</span></span>               | <span data-ttu-id="5491e-119">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="5491e-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="5491e-120">Significado</span><span class="sxs-lookup"><span data-stu-id="5491e-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="5491e-121">DTI</span><span class="sxs-lookup"><span data-stu-id="5491e-121">"P"</span></span>                   | <span data-ttu-id="5491e-122">SDDL \_ protegido</span><span class="sxs-lookup"><span data-stu-id="5491e-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="5491e-123">O sinalizador de SE \_ \_ protegido por DACL está definido.</span><span class="sxs-lookup"><span data-stu-id="5491e-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="5491e-124">MULTI-hop</span><span class="sxs-lookup"><span data-stu-id="5491e-124">"AR"</span></span>                  | <span data-ttu-id="5491e-125">\_req de \_ herança \_ automática de SDDL</span><span class="sxs-lookup"><span data-stu-id="5491e-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="5491e-126">O \_ sinalizador de \_ reherança automática da DACL do se \_ \_ está definido.</span><span class="sxs-lookup"><span data-stu-id="5491e-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="5491e-127">AVANÇADA</span><span class="sxs-lookup"><span data-stu-id="5491e-127">"AI"</span></span>                  | <span data-ttu-id="5491e-128">SDDL \_ auto \_ herdada</span><span class="sxs-lookup"><span data-stu-id="5491e-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="5491e-129">O \_ \_ sinalizador herdado automático do se da DACL \_ está definido.</span><span class="sxs-lookup"><span data-stu-id="5491e-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="5491e-130">"sem \_ controle de acesso \_ "</span><span class="sxs-lookup"><span data-stu-id="5491e-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="5491e-131">\_ACL NULL \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="5491e-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="5491e-132">A ACL é nula.</span><span class="sxs-lookup"><span data-stu-id="5491e-132">The ACL is null.</span></span> <span data-ttu-id="5491e-133">**Windows server 2008, Windows Vista e Windows server 2003:** Não disponível.</span><span class="sxs-lookup"><span data-stu-id="5491e-133">**Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5491e-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sinalizadores de SACL \_</span><span class="sxs-lookup"><span data-stu-id="5491e-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="5491e-135">Sinalizadores de controle do descritor de segurança que se aplicam à SACL.</span><span class="sxs-lookup"><span data-stu-id="5491e-135">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="5491e-136">A \_ cadeia de caracteres de sinalizadores SACL usa as mesmas cadeias de caracteres de bit de controle que a cadeia de sinalizadores DACL \_ .</span><span class="sxs-lookup"><span data-stu-id="5491e-136">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="5491e-137"><span id="string_ace"></span><span id="STRING_ACE"></span>Ace de cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="5491e-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="5491e-138">Uma cadeia de caracteres que descreve uma ACE na DACL ou SACL do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="5491e-138">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="5491e-139">Para obter uma descrição do formato de cadeia de caracteres ACE, consulte [Ace Strings](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5491e-139">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="5491e-140">Cada cadeia de caracteres de ACE é colocada entre parênteses (()).</span><span class="sxs-lookup"><span data-stu-id="5491e-140">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="5491e-141">Os componentes desnecessários podem ser omitidos da cadeia de caracteres do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="5491e-141">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="5491e-142">Por exemplo, se o \_ sinalizador de DACL \_ presente não estiver definido no descritor de segurança de entrada, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) não incluirá um componente D: na cadeia de caracteres de saída.</span><span class="sxs-lookup"><span data-stu-id="5491e-142">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="5491e-143">Você também pode usar os sinalizadores de bit de [**\_ informações de segurança**](security-information.md) para indicar os componentes a serem incluídos em uma cadeia de caracteres de descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="5491e-143">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="5491e-144">O formato de cadeia de caracteres do descritor de segurança não oferece suporte a ACLs **nulas** .</span><span class="sxs-lookup"><span data-stu-id="5491e-144">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="5491e-145">Para indicar uma ACL vazia, a cadeia de caracteres do descritor de segurança inclui o token D: ou S: sem informações de cadeia de caracteres adicionais.</span><span class="sxs-lookup"><span data-stu-id="5491e-145">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="5491e-146">A cadeia de caracteres do descritor de segurança armazena os bits de [**controle do descritor de segurança**](security-descriptor-control.md) de diferentes maneiras.</span><span class="sxs-lookup"><span data-stu-id="5491e-146">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="5491e-147">Os \_ bits da DACL presente \_ ou se a \_ SACL \_ presente são indicados pela presença do token D: ou S: na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5491e-147">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="5491e-148">Outros bits que se aplicam a DACL ou SACL são armazenados em sinalizadores DACL \_ e \_ sinalizadores de SACL.</span><span class="sxs-lookup"><span data-stu-id="5491e-148">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="5491e-149">O proprietário do SE padrão é o padrão do grupo se definido como Default \_ \_ \_ \_ , se a \_ DACL padrão \_ e se \_ \_ os bits padrão da SACL não são armazenados em uma cadeia de caracteres de descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="5491e-149">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="5491e-150">O \_ bit If auto \_ Relative não é armazenado na cadeia de caracteres, mas [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) sempre define esse bit no descritor de segurança de saída.</span><span class="sxs-lookup"><span data-stu-id="5491e-150">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="5491e-151">Os exemplos a seguir mostram as cadeias de caracteres do descritor de segurança e as informações nos descritores de segurança associados.</span><span class="sxs-lookup"><span data-stu-id="5491e-151">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="5491e-152">Cadeia de caracteres 1:</span><span class="sxs-lookup"><span data-stu-id="5491e-152">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="5491e-153">Descritor de segurança 1:</span><span class="sxs-lookup"><span data-stu-id="5491e-153">Security Descriptor 1:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



<span data-ttu-id="5491e-154">Cadeia de caracteres 2:</span><span class="sxs-lookup"><span data-stu-id="5491e-154">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="5491e-155">Descritor de segurança 2:</span><span class="sxs-lookup"><span data-stu-id="5491e-155">Security Descriptor 2:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a><span data-ttu-id="5491e-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5491e-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5491e-157">Cadeias de caracteres ACE</span><span class="sxs-lookup"><span data-stu-id="5491e-157">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="5491e-158">Linguagem de definição do descritor de segurança para ACEs condicionais</span><span class="sxs-lookup"><span data-stu-id="5491e-158">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
