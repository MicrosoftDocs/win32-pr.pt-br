---
description: Para criar um descritor de segurança, um servidor protegido pode usar o mesmo procedimento que um aplicativo usaria para criar um descritor de segurança para um objeto protegível.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descritores de segurança para objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921046"
---
# <a name="security-descriptors-for-private-objects"></a>Descritores de segurança para objetos privados

Para criar um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly), um servidor protegido pode usar o mesmo procedimento que um aplicativo usaria para criar um descritor de segurança para um objeto protegível. Para obter o código de exemplo, consulte [criando um descritor de segurança para um novo objeto em C++](creating-a-security-descriptor-for-a-new-object-in-c--.md). Como alternativa, um aplicativo de servidor protegido pode chamar a função [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) para fazer isso. Se um ponteiro para um [*descritor de segurança autônomo*](/windows/desktop/SecGloss/s-gly) existente for fornecido para **BuildSecurityDescriptor**, ele criará o novo descritor de segurança com informações extraídas do descritor de segurança mesclado com novas informações de controle de acesso passadas como parâmetros na chamada de função. O proprietário e o grupo são opcionalmente especificados por estruturas de [**confiança**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) passadas para a função. O descritor de segurança criado pelo **BuildSecurityDescriptor** está em um formato *auto-relativo* .

Além disso, a API do Windows fornece um conjunto de funções para mesclar informações de segurança do cliente com informações herdadas do descritor de segurança para um objeto pai ou de um descritor de segurança padrão. As funções [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity), [**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity), [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)e [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) fornecem a capacidade de recuperar informações padrão de um [*token de acesso*](/windows/desktop/SecGloss/a-gly), dar suporte à herança e manipular partes específicas do descritor de segurança. Isso pode ser útil quando um cliente cria um objeto particular em uma hierarquia de objetos protegidos. Por exemplo, você pode usar a função **CreatePrivateObjectSecurity** para criar um descritor de segurança que continha ACEs especificadas pelo cliente, Aces herdadas de um objeto pai e o proprietário padrão do token de acesso do cliente de criação. Enquanto o [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) cria descritores de segurança a partir das informações de controle de acesso passadas para a chamada de função ou a partir de uma descrição de segurança existente, o **CreatePrivateObjectSecurity** cria um descritor de segurança exclusivamente das informações nos descritores de segurança existentes.

A função [**LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) Obtém informações de descritor de segurança de um [*descritor de segurança autônomo*](/windows/desktop/SecGloss/s-gly)existente. Essas informações incluem a especificação de proprietário e de grupo, o número de ACEs na SACL ou DACL e a lista de ACEs na SACL ou DACL.

 

 
