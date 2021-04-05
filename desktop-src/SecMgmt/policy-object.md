---
description: O objeto de política é usado para controlar o acesso ao banco de dados da autoridade de segurança local (LSA) e contém informações que se aplicam ao sistema inteiro ou estabelecem padrões para o sistema.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Objeto de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826981"
---
# <a name="policy-object"></a>Objeto de política

O objeto de **política** é usado para controlar o acesso ao banco de dados da [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) e contém informações que se aplicam ao sistema inteiro ou estabelecem padrões para o sistema. Cada sistema tem apenas um objeto de **política** . Esse objeto de **política** é criado pela LSA quando o sistema é iniciado e os aplicativos não podem criá-lo ou destruí-lo.

As informações armazenadas em um objeto de **política** incluem:

-   Cota de memória padrão do sistema. A menos que especificado de outra forma, cada usuário que fizer logon no sistema receberá essa cota de memória. Cotas de memória especiais podem ser atribuídas a indivíduos ou membros de grupos ou grupos locais por meio de um objeto de [**conta**](account-object.md) .
-   Requisitos de auditoria de segurança em todo o sistema.
-   O nome e o SID do domínio da conta deste sistema.
-   Informações sobre o domínio primário deste sistema. Essas informações incluem o nome e o SID do domínio primário, o nome da conta no domínio primário que deve ser usado para solicitações de autenticação, traduções de nome e SID e a obtenção dos nomes dos controladores de domínio no domínio. Esses nomes podem estar desatualizados e devem ser levados apenas em uma dica. A ordem dessa lista é considerada significativa e será mantida. Isso permite, por exemplo, o primeiro nome na lista para representar o último controlador de domínio primário conhecido.
-   Informações sobre se a LSA contém a cópia mestra das informações de política ou uma réplica. Somente parte das informações de política é replicada; o restante é estabelecido em uma base por sistema.

Os campos **AccountDomain** e **PrimaryDomain** do objeto de **política** são usados para finalidades diferentes, dependendo do tipo de relações de confiança e do sistema:

-   Em um sistema que não tem um domínio primário, o campo **AccountDomain** contém o nome e o SID do domínio de conta local do sistema, que é o mesmo que o nome do computador. O campo **PrimaryDomain** contém o nome do grupo de trabalho do qual este computador é membro. Os objetos [**TrustedDomain**](trusteddomain-object.md) são ignorados com uma exceção – não pode haver um objeto **TrustedDomain** com o mesmo nome que o grupo de trabalho, pois ele será exibido como se fosse o domínio primário do computador.
-   Em um sistema que tem um domínio primário, o campo **AccountDomain** identifica o nome e o SID do domínio da conta local, como antes. No entanto, o campo **PrimaryDomain** contém o nome e o SID do domínio primário para o sistema. Além disso, deve haver um objeto [**TrustedDomain**](trusteddomain-object.md) com o nome e o Sid identificados no campo **PrimaryDomain** . Esse objeto **TrustedDomain** contém as informações de conta e servidor necessárias para estabelecer um canal seguro para um controlador de domínio no domínio primário. Todos os outros objetos **TrustedDomain** são ignorados.
-   Em controladores de domínio, o campo **AccountDomain** identifica o domínio de conta local para o sistema; no entanto, o nome da conta é atribuído pelo usuário em vez de ser um nome conhecido. Como o domínio primário é o mesmo que o domínio da conta, o campo **PrimaryDomain** deve conter o mesmo valor que o campo **AccountDomain** . Além disso, espera-se que todos os objetos [**TrustedDomain**](trusteddomain-object.md) sejam válidos e representem relações de confiança com outros domínios. Se o sistema não confiar em nenhum outro domínio, não deverá haver nenhum objeto **TrustedDomain** .

 

 
