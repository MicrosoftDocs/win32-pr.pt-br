---
description: Você pode atribuir privilégios a contas usando o snap-in do MMC (console de gerenciamento Microsoft) da política de segurança local (secpol. msc) ou chamando a função LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Atribuindo privilégios a uma conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753237"
---
# <a name="assigning-privileges-to-an-account"></a>Atribuindo privilégios a uma conta

Você pode atribuir privilégios a contas usando o snap-in do MMC (console de gerenciamento Microsoft) da política de segurança local (secpol. msc) ou chamando a função [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .

A atribuição de um privilégio a uma conta não afeta os tokens de usuário existentes. Um usuário deve fazer logoff e, em seguida, fazer logon novamente para obter um token de acesso com o privilégio atribuído recentemente.

Para atribuir privilégios usando o snap-in de política de segurança local do MMC, edite a lista de usuários para cada privilégio listado em **configurações de segurança/políticas locais/atribuição de direitos de usuário**.

 

 
