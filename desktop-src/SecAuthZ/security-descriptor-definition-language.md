---
description: Explica a SDDL (linguagem de definição do descritor de segurança).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Linguagem de definição do descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b72e74f49d34577251aef3d875a3c0e9aede07556be1b918ad532f3987c54d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907406"
---
# <a name="security-descriptor-definition-language"></a>Linguagem de definição do descritor de segurança

A SDDL (linguagem de definição do descritor de segurança) define o formato de cadeia de caracteres que as funções [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usam para descrever um [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança como uma cadeia de caracteres de texto. A linguagem também define elementos de cadeia de caracteres para descrever informações nos componentes de um descritor de segurança.

> [!Note]  
> As ACEs [*(entradas de controle*](/windows/desktop/SecGloss/a-gly) de acesso condicional) têm um formato SDDL diferente de outros tipos ACE. Para ACEs, consulte [Cadeias de caracteres ACE.](ace-strings.md) Para ACEs condicionais, consulte [Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de cadeia de caracteres do descritor de segurança](security-descriptor-string-format.md)
</dt> <dt>

[Linguagem de definição do descritor de segurança para ACEs condicionais](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[Cadeias de Caracteres ACE](ace-strings.md)
</dt> <dt>

[Cadeias de Caracteres SID](sid-strings.md)
</dt> <dt>

[\[MS-DTYP: \] linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
