---
title: Agente do sistema de diretório
description: O Directory System Agent (DSA) é uma coleção de serviços e processos que são executados em cada controlador de domínio e fornecem acesso ao armazenamento de dados.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Directory System Agent Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823665"
---
# <a name="directory-system-agent"></a>Agente do sistema de diretório

O [*Directory System Agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) é uma coleção de serviços e processos que são executados em cada controlador de domínio e fornecem acesso ao armazenamento de dados. O armazenamento de dados é o repositório físico de dados de diretório localizados em um disco rígido. No Active Directory Domain Services, o DSA faz parte do subsistema da autoridade do sistema local (LSA). Os clientes acessam o diretório usando um dos seguintes mecanismos com suporte no DSA:

-   Os clientes LDAP se conectam ao DSA usando o LDAP (Lightweight Directory Access Protocol). O Active Directory Domain Services dá suporte ao LDAP 3,0, definido pela RFC 3377 e pelo LDAP 2,0, definido pela RFC 1777. Os clientes Windows usam o LDAP 3,0 para se conectar ao DSA.
-   Clientes MAPI, como o Microsoft Exchange Server, se conectam ao DSA usando a interface de chamada de procedimento remoto MAPI.
-   Os DSAs no Active Directory Domain Services se conectam entre si para executar a replicação usando uma interface de chamada de procedimento remoto proprietário.

 

 