---
description: O objeto Policy é usado para controlar o acesso ao banco de dados da LSA (Autoridade de Segurança Local) e contém informações que se aplica a todo o sistema ou estabelece padrões para o sistema.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Objeto Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49e3dd7a33fd83107f9338783e3b8bdcc68eee7d8c4f927f67a7df1c0262c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005054"
---
# <a name="policy-object"></a>Objeto Policy

O **objeto Policy** é usado para controlar o acesso ao banco de dados da LSA (Autoridade de Segurança [*Local)*](/windows/desktop/SecGloss/l-gly) e contém informações que se aplica a todo o sistema ou estabelece padrões para o sistema. Cada sistema tem apenas um **objeto Policy.** Esse **objeto** Policy é criado pelo LSA quando o sistema é iniciado e os aplicativos não podem criar ou destruir.

As informações armazenadas em um **objeto Policy** incluem:

-   Cota de memória padrão do sistema. A menos que especificado de outra forma, cada usuário que fazer logo no sistema receberá essa cota de memória. Cotas de memória especiais podem ser atribuídas a indivíduos ou membros de grupos ou grupos locais por meio de [**um objeto**](account-object.md) Account.
-   Requisitos de auditoria de segurança em todo o sistema.
-   O nome e o SID do domínio da conta desse sistema.
-   Informações sobre o domínio primário desse sistema. Essas informações incluem o nome e o SID do domínio primário, o nome da conta dentro do domínio primário que deve ser usado para solicitações de autenticação, traduções de nome e SID e obtenção dos nomes de controladores de domínio dentro do domínio. Esses nomes podem estar des date e devem ser tomadas apenas como uma dica. A ordem dessa lista é assumida como significativa e será mantida. Isso permite, por exemplo, que o primeiro nome na lista represente o último controlador de domínio primário conhecido.
-   Informações sobre se o LSA contém a cópia mestra das informações da política ou uma réplica. Somente parte das informações da política é replicada; o restante é estabelecido por sistema.

Os **campos AccountDomain** e **PrimaryDomain** do objeto **Policy** são usados para finalidades diferentes, dependendo do tipo de sistema e relações de confiança:

-   Em um sistema que não tem um domínio primário, o campo **AccountDomain** contém o nome e o SID do domínio da conta local do sistema, que é o mesmo que o nome do computador. O **campo PrimaryDomain** contém o nome do grupo de trabalho de que este computador é membro. [**Objetos TrustedDomain**](trusteddomain-object.md) são ignorados com uma exceção — não pode haver um objeto **TrustedDomain** com o mesmo nome que o grupo de trabalho, pois ele será exibido como se fosse o domínio primário do computador.
-   Em um sistema que tem um domínio primário, o **campo AccountDomain** identifica o nome e o SID do domínio da conta local, como antes. No entanto, **o campo PrimaryDomain** contém o nome e o SID do domínio primário do sistema. Além disso, deve haver um objeto [**TrustedDomain**](trusteddomain-object.md) com o nome e o SID identificados no **campo PrimaryDomain.** Esse **objeto TrustedDomain** contém as informações de conta e servidor necessárias para estabelecer um canal seguro para um controlador de domínio no domínio primário. Todos os **outros objetos TrustedDomain** são ignorados.
-   Em controladores de domínio, **o campo AccountDomain** identifica o domínio da conta local para o sistema; no entanto, o nome da conta é atribuído pelo usuário em vez de ser um nome conhecido. Como o domínio primário é o mesmo que o domínio da conta, o **campo PrimaryDomain** deve conter o mesmo valor que o **campo AccountDomain.** Além disso, todos [**os objetos TrustedDomain**](trusteddomain-object.md) devem ser válidos e representar relações de confiança com outros domínios. Se o sistema não confiar em nenhum outro domínio, não deverá haver nenhum **objeto TrustedDomain.**

 

 
