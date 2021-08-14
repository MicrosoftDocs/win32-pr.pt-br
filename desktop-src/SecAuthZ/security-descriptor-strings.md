---
description: Um descritor de segurança funcional válido contém informações de segurança em formato binário.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Cadeia de caracteres do descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413786"
---
# <a name="security-descriptor-strings"></a>Cadeia de caracteres do descritor de segurança

Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) funcional válido contém informações de segurança em formato binário. a API Windows fornece funções para converter descritores de segurança binários de e para cadeias de caracteres de texto. Os descritores de segurança no formato de cadeia de caracteres não são funcionais, mas podem ser úteis para armazenar ou transportar informações de descrição de segurança.

Para converter um descritor de segurança em um formato de cadeia de caracteres, chame a função [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) . Para converter um descritor de segurança de formato de cadeia de caracteres de volta para um descritor de segurança funcional válido, chame a função [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .

Para obter mais informações, consulte [linguagem de definição do descritor de segurança](security-descriptor-definition-language.md).

 

 
