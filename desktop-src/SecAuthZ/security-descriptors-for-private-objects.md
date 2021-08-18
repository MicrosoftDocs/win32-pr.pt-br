---
description: Para criar um descritor de segurança, um servidor protegido pode usar o mesmo procedimento que um aplicativo usaria para criar um descritor de segurança para um objeto protegível.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descritores de segurança para objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bae6615f309e572dc2e22f76310ccdf84bbbf5fff504aef0331d7d8e6b60ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413726"
---
# <a name="security-descriptors-for-private-objects"></a>Descritores de segurança para objetos privados

Para criar um [*descritor de*](/windows/desktop/SecGloss/s-gly)segurança, um servidor protegido pode usar o mesmo procedimento que um aplicativo usaria para criar um descritor de segurança para um objeto protegível. Para o código de exemplo, [consulte Criando um descritor de segurança para um novo objeto em C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md) Como alternativa, um aplicativo de servidor protegido pode chamar a [**função BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) para fazer isso. Se um ponteiro para [](/windows/desktop/SecGloss/s-gly) um descritor de segurança auto-relativo existente for fornecido para **BuildSecurityDescriptor**, ele criará o novo descritor de segurança com informações retiradas desse descritor de segurança mescladas com novas informações de controle de acesso passadas como parâmetros na chamada de função. O proprietário e o grupo são opcionalmente especificados por estruturas [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) passadas para a função. O descritor de segurança criado por **BuildSecurityDescriptor** está no *formato auto-relativo.*

Além disso, a API Windows fornece um conjunto de funções para mesclar informações de segurança do cliente com informações herdadas do descritor de segurança para um objeto pai ou de um descritor de segurança padrão. As funções [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity), [**GetPrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity) [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)e [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) fornecem a capacidade de recuperar informações padrão de um [*token*](/windows/desktop/SecGloss/a-gly)de acesso, dar suporte à herança e manipular partes específicas do descritor de segurança. Isso pode ser útil quando um cliente cria um objeto privado em uma hierarquia de objetos protegidos. Por exemplo, você pode usar a função **CreatePrivateObjectSecurity** para criar um descritor de segurança que continha ACEs especificadas pelo cliente, ACEs herdadas de um objeto pai e o proprietário padrão do token de acesso do cliente de criação. Embora [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crie descritores de segurança de informações de controle de acesso passadas para a chamada de função ou de um descritor de segurança existente, **CreatePrivateObjectSecurity** cria um descritor de segurança exclusivamente com base nas informações em descritores de segurança existentes.

[**A função LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) obtém informações do descritor de segurança de um [*descritor de segurança auto-relativo existente.*](/windows/desktop/SecGloss/s-gly) Essas informações incluem a especificação de proprietário e grupo, o número de ACEs na SACL ou DACL e a lista de ACEs no SACL ou NACL.

 

 
