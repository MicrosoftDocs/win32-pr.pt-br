---
description: Funções para criar um descritor de segurança e obter e definir os componentes de um descritor de segurança.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Criação de descritor de segurança de nível baixo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781479"
---
# <a name="low-level-security-descriptor-creation"></a>Criação de descritor de segurança de nível baixo

O controle de acesso de nível baixo fornece um conjunto de funções para criar um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) e obter e definir os componentes de um descritor de segurança. As funções de nível baixo para inicializar e definir os componentes de um descritor de segurança só funcionam com os descritores de segurança de formato absoluto. As funções de nível baixo para obter os componentes de um descritor de segurança funcionam com os descritores de [segurança absolutos e autônomos](absolute-and-self-relative-security-descriptors.md).

A função [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) Inicializa um buffer de [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) . O descritor de segurança inicializado está em formato [*absoluto*](/windows/desktop/SecGloss/a-gly) e não tem proprietário, grupo primário, [*lista de controle de acesso discricional*](/windows/desktop/SecGloss/d-gly) (DACL) ou [*lista de controle de acesso do sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Você pode usar as seguintes funções de baixo nível para obter ou definir componentes específicos de um descritor de segurança especificado.



| Função                                                             | Descrição                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Recupera informações de revisão e controle de um descritor de segurança.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Recupera a DACL de um descritor de segurança.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Recupera o Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) do grupo primário de um descritor de segurança. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Retorna o comprimento de um descritor de segurança.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Recupera o SID do proprietário de um descritor de segurança.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Recupera a SACL de um descritor de segurança.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Coloca uma DACL em um descritor de segurança, substituindo qualquer DACL existente.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Define o SID do grupo primário de um descritor de segurança.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Define o SID do proprietário de um descritor de segurança.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Coloca uma SACL em um descritor de segurança, substituindo qualquer SACL existente.                                                                                                    |



 

Para verificar o nível de revisão e a [*integridade*](/windows/desktop/SecGloss/i-gly) estrutural de um descritor de segurança, chame a função [**IsValidSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) .

 

 
