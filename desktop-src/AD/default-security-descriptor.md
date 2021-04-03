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
# <a name="default-security-descriptor"></a>Descritor de segurança padrão

Com Active Directory Domain Services, você também pode especificar a segurança padrão para cada tipo de objeto. Isso é especificado no atributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) na definição do objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) no esquema de [Active Directory](active-directory-schema.md). Esse descritor de segurança é usado para fornecer proteção padrão no objeto se não houver descritor de segurança especificado durante a criação do objeto.

> [!Note]  
> As ACEs de um descritor de segurança padrão são manipuladas como se fossem especificadas como parte da criação do objeto. Portanto, as ACEs padrão são colocadas antes das ACEs herdadas e as substituem conforme apropriado. Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

O [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) é especificado em um formato de cadeia de caracteres especial usando o SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ). Duas funções podem ser usadas para converter a forma binária do descritor de segurança para o formato de cadeia de caracteres e vice-versa. Essas funções são:

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Para obter mais informações e os descritores de segurança padrão das classes de objeto predefinidas, consulte as páginas de referência de classe na referência de esquema de Active Directory da [referência de Active Directory Domain Services](active-directory-domain-services-reference.md).

Para obter mais informações e um exemplo de código que lê ou modifica a propriedade [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de uma classe de objeto, consulte [lendo o DefaultSecurityDescriptor para uma classe de objeto](reading-the-defaultsecuritydescriptor-for-an-object-class.md) e [modificando o DefaultSecurityDescriptor para uma classe de objeto](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).

 

 