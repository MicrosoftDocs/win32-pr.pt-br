---
title: Descritor de segurança padrão
description: Com Active Directory Domain Services, você também pode especificar a segurança padrão para cada tipo de objeto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- AD do descritor de segurança padrão
- descritores de segurança AD , padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed57b775196ad6981a88b5621076d76c61035c4700af25ed3f35703fc9018b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019877"
---
# <a name="default-security-descriptor"></a>Descritor de segurança padrão

Com Active Directory Domain Services, você também pode especificar a segurança padrão para cada tipo de objeto. Isso é especificado no atributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) na definição de objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) no [esquema do Active Directory](active-directory-schema.md). Esse descritor de segurança é usado para fornecer proteção padrão no objeto se não houver nenhum descritor de segurança especificado durante a criação do objeto.

> [!Note]  
> As ACEs de um descritor de segurança padrão são tratadas como se fossem especificadas como parte da criação do objeto. Portanto, as ACEs padrão são colocadas antes das ACEs herdadas e as substituem conforme apropriado. Para obter mais informações, [consulte Ordem de ACEs em um DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

O [**defaultSecurityDescriptor é**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) especificado em um formato de cadeia de caracteres especial usando a SDDL [(Linguagem](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de Definição do Descritor de Segurança). Duas funções podem ser usadas para converter a forma binária do descritor de segurança em formato de cadeia de caracteres e vice-versa. Essas funções são:

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Para obter mais informações e os descritores de segurança padrão das classes de objeto predefinidas, consulte as páginas de referência de classe na Referência de esquema do Active Directory do [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).

Para obter mais informações e um exemplo de código que lê ou modifica a propriedade [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de uma classe de objeto, consulte Lendo o [defaultSecurityDescriptor para](reading-the-defaultsecuritydescriptor-for-an-object-class.md) uma Classe de Objeto e Modificando o [defaultSecurityDescriptor](modifying-the-defaultsecuritydescriptor-for-an-object-class.md)para uma classe de objeto .

 

 