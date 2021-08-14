---
title: Como os grupos de segurança são usados no controle de acesso
description: O SID (identificador de segurança) é o identificador de objeto do usuário ou grupo de segurança quando o usuário ou grupo é usado para fins de segurança.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Como os grupos de segurança são usados no controle de acesso
- controle de acesso, grupos de segurança usados no
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8e14d4d8c371d07619d93f4a6d06318f91e7ec011a4c4fe6d436074ac8ff94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188127"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Como os grupos de segurança são usados no controle de acesso

O SID (identificador de segurança) é o identificador de objeto do usuário ou grupo de segurança quando o usuário ou grupo é usado para fins de segurança. O nome do usuário ou grupo não é usado como o identificador exclusivo dentro do sistema. O SID é armazenado no atributo **objectSid** de objetos de usuário e objetos de grupo de segurança. O servidor do Active Directory gera **o objectSid** quando o usuário ou grupo é criado. O sistema garante que os SIDs sejam exclusivos em uma floresta. Esteja ciente de que **o objectGuid** é o identificador exclusivo de um usuário, grupo ou qualquer outro objeto de diretório. O SID muda se um usuário ou grupo é movido para outro domínio; o **objectGuid** permanece o mesmo.

Quando um usuário ou grupo recebe permissão para acessar um recurso, como uma impressora ou um compartilhamento de arquivos, o SID do usuário ou grupo é adicionado à ACE (entrada de controle de acesso) definindo a permissão concedida na DACL (lista de controle de acesso discricionário) do recurso. No Active Directory Domain Services, cada objeto tem um atributo **nTSecurityDescriptor** que armazena uma DACL que define o acesso a esse objeto ou atributos específicos nesse objeto. Para obter mais informações sobre como definir o controle de acesso em objetos Active Directory Domain Services, consulte [Controlando](controlling-access-to-objects-in-active-directory-domain-services.md)o acesso a objetos no Active Directory Domain Services .

Quando um usuário faz login em um domínio Windows 2000, o sistema operacional gera um token de acesso. Esse token de acesso é usado para determinar quais recursos o usuário pode acessar. O token de acesso do usuário inclui os seguintes dados:

-   SID do usuário.
-   SIDs de todos os grupos de segurança globais e universais dos que o usuário é membro.
-   SIDs de todos os grupos de segurança globais e universais aninhados.

Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.

Quando o usuário tenta acessar recursos em um computador, o serviço por meio do qual o usuário acessa o recurso representará o usuário criando um novo token de acesso com base no token de acesso criado no momento do logon do usuário. Esse novo token de acesso também conterá os seguintes SIDs:

-   SIDs para todos os grupos locais de domínio no domínio de destino do que o usuário é membro.
-   SIDs para todos os grupos locais do computador no computador de destino do que o usuário é membro.

O serviço usa esse novo token de acesso para avaliar o acesso ao recurso. Se um SID no token de acesso aparecer em qualquer ACEs na DACL, o serviço dará ao usuário as permissões especificadas nessas ACEs.

 

 




