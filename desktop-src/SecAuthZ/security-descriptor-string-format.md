---
description: O formato de cadeia de caracteres do descritor de segurança é um formato de texto para armazenar ou transportar informações em um descritor de segurança.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Formato de cadeia de caracteres descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827334"
---
# <a name="security-descriptor-string-format"></a>Formato de cadeia de caracteres descritor de segurança

O **formato de cadeia de caracteres do descritor de segurança** é um formato de texto para armazenar ou transportar informações em um descritor de segurança. As funções [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usam esse formato.

O formato é uma cadeia de caracteres terminada em **nulo** com tokens para indicar cada um dos quatro componentes principais de um descritor de segurança: proprietário (O:), grupo primário (G:), DACL (D:) e SACL (S:).

> [!Note]  
> [*As*](/windows/desktop/SecGloss/a-gly) ACEs (entradas de controle de acesso) e as ACEs condicionais têm formatos diferentes. Para ACEs, consulte [seqüências de caracteres Ace](ace-strings.md). Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>Sid do proprietário \_
</dt> <dd>

Uma [cadeia de caracteres Sid](sid-strings.md) que identifica o proprietário do objeto.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>Sid do grupo \_
</dt> <dd>

Uma cadeia de caracteres SID que identifica o grupo primário do objeto.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>sinalizadores de DACL \_
</dt> <dd>

Sinalizadores de controle do descritor de segurança que se aplicam à DACL. Para obter uma descrição desses sinalizadores de controle, consulte a função [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . A \_ cadeia de caracteres de sinalizadores DACL pode ser uma concatenação de zero ou mais das cadeias de caracteres a seguir.



| Control               | Constante em SDDL. h       | Significado                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| DTI                   | SDDL \_ protegido          | O sinalizador de SE \_ \_ protegido por DACL está definido.          |
| MULTI-hop                  | \_req de \_ herança \_ automática de SDDL | O \_ sinalizador de \_ reherança automática da DACL do se \_ \_ está definido. |
| AVANÇADA                  | SDDL \_ auto \_ herdada    | O \_ \_ sinalizador herdado automático do se da DACL \_ está definido.    |
| "sem \_ controle de acesso \_ " | \_ACL nula de SSDL \_          | A ACL é nula.                              |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sinalizadores de SACL \_
</dt> <dd>

Sinalizadores de controle do descritor de segurança que se aplicam à SACL. A \_ cadeia de caracteres de sinalizadores SACL usa as mesmas cadeias de caracteres de bit de controle que a cadeia de sinalizadores DACL \_ .

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>Ace de cadeia de caracteres \_
</dt> <dd>

Uma cadeia de caracteres que descreve uma ACE na DACL ou SACL do descritor de segurança. Para obter uma descrição do formato de cadeia de caracteres ACE, consulte [Ace Strings](ace-strings.md). Cada cadeia de caracteres de ACE é colocada entre parênteses (()).

</dd> </dl>

Os componentes desnecessários podem ser omitidos da cadeia de caracteres do descritor de segurança. Por exemplo, se o \_ sinalizador de DACL \_ presente não estiver definido no descritor de segurança de entrada, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) não incluirá um componente D: na cadeia de caracteres de saída. Você também pode usar os sinalizadores de bit de [**\_ informações de segurança**](security-information.md) para indicar os componentes a serem incluídos em uma cadeia de caracteres de descritor de segurança.

O formato de cadeia de caracteres do descritor de segurança não oferece suporte a ACLs **nulas** .

Para indicar uma ACL vazia, a cadeia de caracteres do descritor de segurança inclui o token D: ou S: sem informações de cadeia de caracteres adicionais.

A cadeia de caracteres do descritor de segurança armazena os bits de [**controle do descritor de segurança**](security-descriptor-control.md) de diferentes maneiras. Os \_ bits da DACL presente \_ ou se a \_ SACL \_ presente são indicados pela presença do token D: ou S: na cadeia de caracteres. Outros bits que se aplicam a DACL ou SACL são armazenados em sinalizadores DACL \_ e \_ sinalizadores de SACL. O proprietário do SE padrão é o padrão do grupo se definido como Default \_ \_ \_ \_ , se a \_ DACL padrão \_ e se \_ \_ os bits padrão da SACL não são armazenados em uma cadeia de caracteres de descritor de segurança. O \_ bit If auto \_ Relative não é armazenado na cadeia de caracteres, mas [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) sempre define esse bit no descritor de segurança de saída.

Os exemplos a seguir mostram as cadeias de caracteres do descritor de segurança e as informações nos descritores de segurança associados.

Cadeia de caracteres 1:


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



Descritor de segurança 1:


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



Cadeia de caracteres 2:


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



Descritor de segurança 2:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cadeias de caracteres ACE](ace-strings.md)
</dt> <dt>

[Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
