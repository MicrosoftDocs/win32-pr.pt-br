---
description: Funções para criar um descritor de segurança e obter e definir os componentes de um descritor de segurança.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Criação de descritor de segurança de baixo nível
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781479"
---
# <a name="low-level-security-descriptor-creation"></a>Criação de descritor de segurança de baixo nível

O controle de acesso de baixo nível fornece um conjunto de funções para criar um descritor [*de*](/windows/desktop/SecGloss/s-gly) segurança e obter e definir os componentes de um descritor de segurança. As funções de baixo nível para inicializar e definir os componentes de um descritor de segurança funcionam apenas com descritores de segurança de formato absoluto. As funções de baixo nível para obter os componentes de um descritor de segurança funcionam com descritores de segurança [absolutos e auto-relativos.](absolute-and-self-relative-security-descriptors.md)

A [**função InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) inicializa um buffer [**SECURITY \_ DESCRIPTOR.**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) O descritor de segurança [](/windows/desktop/SecGloss/a-gly) inicializado está em formato absoluto e não tem proprietário, grupo [*primário,*](/windows/desktop/SecGloss/d-gly) DACL (lista de controle de acesso discricionário) ou SACL (lista de controle de acesso [*do*](/windows/desktop/SecGloss/s-gly) sistema). Você pode usar as funções de baixo nível a seguir para obter ou definir componentes específicos de um descritor de segurança especificado.



| Função                                                             | Descrição                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Recupera informações de revisão e controle de um descritor de segurança.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Recupera a DACL de um descritor de segurança.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Recupera o SID [*(identificador de*](/windows/desktop/SecGloss/s-gly) segurança) do grupo primário de um descritor de segurança. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Retorna o comprimento de um descritor de segurança.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Recupera o SID do proprietário de um descritor de segurança.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Recupera a SACL de um descritor de segurança.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Coloca uma DACL em um descritor de segurança, superando qualquer DACL existente.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Define o SID do grupo primário de um descritor de segurança.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Define o SID do proprietário de um descritor de segurança.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Coloca uma SACL em um descritor de segurança, superando qualquer SACL existente.                                                                                                    |



 

Para verificar o nível de revisão [*e*](/windows/desktop/SecGloss/i-gly) a integridade estrutural de um descritor de segurança, chame a [**função IsValidSecurityDescriptor.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor)

 

 
