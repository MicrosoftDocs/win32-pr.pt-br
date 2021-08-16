---
description: Use as funções GetSecurityInfo e GetNamedSecurityInfo para recuperar um ponteiro para um descritor de segurança de objetos.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Operações do descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c7a7d1dab22f27bad785c6e1394403588a1719b2cc29932aba909aec89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780125"
---
# <a name="security-descriptor-operations"></a>Operações do descritor de segurança

a API de Windows fornece funções para obter e definir os componentes do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) associado a um objeto protegível. Use as funções [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para recuperar um ponteiro para um descritor de segurança de um objeto. Essas funções também podem recuperar ponteiros para os componentes individuais do descritor de segurança: DACL, SACL, SID de proprietário e SID de grupo primário. Use as funções [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para definir os componentes do descritor de segurança de um objeto.

Em geral, você deve usar [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) com objetos identificados por um identificador e [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) com objetos identificados por um nome. Para obter mais informações sobre as funções específicas a serem usadas ao trabalhar com os vários tipos de objetos, consulte [objetos protegíveis](securable-objects.md).

a API de Windows fornece funções adicionais para manipular os componentes de um descritor de segurança. Para obter informações sobre como trabalhar com listas de controle de acesso (DACLs ou SACLs), consulte [obtendo informações de uma ACL](getting-information-from-an-acl.md) e [criando ou modificando uma ACL](creating-or-modifying-an-acl.md). Para obter informações sobre SIDs, consulte SIDs ( [identificadores de segurança](security-identifiers.md) ).

Para obter as informações de controle em um descritor de segurança, chame a função [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Para definir os bits de controle relacionados à herança de ACE automática, chame a função [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . Outros bits de controle são definidos pelas várias funções que definem um componente de descritor de segurança. Por exemplo, se você usar [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) para alterar a DACL de um objeto, a função definirá ou desmarcará os bits conforme apropriado para indicar se o descritor de segurança tem uma DACL, se é uma DACL padrão e assim por diante. Outro exemplo é o bits de controle do [*Gerenciador de recursos*](/windows/desktop/SecGloss/r-gly) (RM) contido no descritor de segurança. Esses bits são usados de acordo com a implementação do Gerenciador de recursos e são acessados por meio das funções [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) e [**SetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) .

 

 
