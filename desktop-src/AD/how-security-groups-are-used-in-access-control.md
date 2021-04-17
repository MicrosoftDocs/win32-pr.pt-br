---
title: Como os grupos de segurança são usados no controle de acesso
description: O SID (identificador de segurança) é o identificador de objeto do usuário ou grupo de segurança quando o usuário ou grupo é usado para fins de segurança.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Como os grupos de segurança são usados no controle de acesso
- controle de acesso, grupos de segurança usados em
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753039"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Como os grupos de segurança são usados no controle de acesso

O SID (identificador de segurança) é o identificador de objeto do usuário ou grupo de segurança quando o usuário ou grupo é usado para fins de segurança. O nome do usuário ou grupo não é usado como o identificador exclusivo no sistema. O SID é armazenado no atributo **objectSid** de objetos de usuário e objetos de grupo de segurança. O servidor de Active Directory gera o **objectSid** quando o usuário ou grupo é criado. O sistema garante que os SIDs sejam exclusivos em uma floresta. Lembre-se de que **objectGUID** é o identificador exclusivo de um usuário, grupo ou qualquer outro objeto de diretório. O SID será alterado se um usuário ou grupo for movido para outro domínio; o **objectGUID** permanece o mesmo.

Quando um usuário ou grupo recebe permissão para acessar um recurso, como uma impressora ou um compartilhamento de arquivos, o SID do usuário ou grupo é adicionado à ACE (entrada de controle de acesso) que define a permissão concedida na DACL (lista de controle de acesso discricionário) do recurso. Em Active Directory Domain Services, cada objeto tem um atributo **nTSecurityDescriptor** que armazena uma DACL definindo o acesso a esse objeto ou atributos específicos nesse objeto. Para obter mais informações sobre como definir o controle de acesso em objetos no Active Directory Domain Services, consulte [controlando o acesso a objetos no Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Quando um usuário faz logon em um domínio do Windows 2000, o sistema operacional gera um token de acesso. Esse token de acesso é usado para determinar quais recursos o usuário pode acessar. O token de acesso do usuário inclui os seguintes dados:

-   SID do usuário.
-   SIDs de todos os grupos de segurança globais e universais dos quais o usuário é membro.
-   SIDs de todos os grupos de segurança global e universal aninhados.

Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.

Quando o usuário tenta acessar recursos em um computador, o serviço pelo qual o usuário acessa o recurso representará o usuário criando um novo token de acesso com base no token de acesso criado no momento do logon do usuário. Esse novo token de acesso também conterá os seguintes SIDs:

-   SIDs para todos os grupos locais de domínio no domínio de destino do qual o usuário é membro.
-   SIDs para todos os grupos locais de computador no computador de destino do qual o usuário é membro.

O serviço usa esse novo token de acesso para avaliar o acesso ao recurso. Se um SID no token de acesso aparecer em quaisquer ACEs na DACL, o serviço fornecerá ao usuário as permissões especificadas nessas ACEs.

 

 




