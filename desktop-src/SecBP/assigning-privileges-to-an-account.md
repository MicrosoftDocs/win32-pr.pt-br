---
description: Você pode atribuir privilégios a contas usando o snap-in da Política de Segurança Console de Gerenciamento Microsoft Local (MMC) (Secpol.msc) ou chamando a função LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Atribuindo privilégios a uma conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ba4fb5266a66aac67b17c70fc6bbcaa1a397a8593534144c688daaee5a0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623006"
---
# <a name="assigning-privileges-to-an-account"></a>Atribuindo privilégios a uma conta

Você pode atribuir privilégios a contas usando o snap-in da Política de Segurança Console de Gerenciamento Microsoft Local (MMC) (Secpol.msc) ou chamando a [**função LsaAddAccountRights.**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights)

Atribuir um privilégio a uma conta não afeta os tokens de usuário existentes. Um usuário deve fazer logoff e, em seguida, fazer logoff novamente para obter um token de acesso com o privilégio recém-atribuído.

Para atribuir privilégios usando o snap-in MMC da Política de Segurança Local, edite a lista de usuários para cada privilégio listado em Segurança **Configurações/Políticas Locais/Atribuição** de Direitos de Usuário .

 

 
