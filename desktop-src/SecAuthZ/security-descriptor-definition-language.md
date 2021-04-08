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
# <a name="security-descriptor-definition-language"></a>Linguagem de definição do descritor de segurança

O SDDL (Security Descriptor Definition Language) define o formato de cadeia de caracteres que as funções [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usam para descrever um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) como uma cadeia de texto. O idioma também define elementos de cadeia de caracteres para descrever informações nos componentes de um descritor de segurança.

> [!Note]  
> As ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) condicional) têm um formato SDDL diferente dos outros tipos ACE. Para ACEs, consulte [seqüências de caracteres Ace](ace-strings.md). Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de cadeia de caracteres descritor de segurança](security-descriptor-string-format.md)
</dt> <dt>

[Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[Cadeias de caracteres ACE](ace-strings.md)
</dt> <dt>

[Cadeias de caracteres de SID](sid-strings.md)
</dt> <dt>

[\[MS-DTYP \] : linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
