---
title: Decidindo onde pesquisar
description: Este tópico explica as diferentes pesquisas que podem ser executadas em Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidindo onde pesquisar o AD
- Active Directory AD , pesquisando, decidindo onde pesquisar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6984a79bb761c1926b6735a91209c9f387ac45619ffc752daef253a74f5e587a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024314"
---
# <a name="deciding-where-to-search"></a>Decidindo onde pesquisar

Este tópico explica as diferentes pesquisas que podem ser executadas em Active Directory Domain Services.

Todas as pesquisas são executadas em um dos seguintes contextos de nomeação:

-   Domínio, incluindo partições de diretório do aplicativo
-   Contêiner de esquema
-   Contêiner de configuração
-   Catálogo global

## <a name="searching-a-domain"></a>Pesquisando um domínio

Os domínios contêm a maioria dos objetos altamente usados, como usuários, contatos, grupos, unidades organizacionais, computadores e assim por diante. A maioria das consultas pesquisa um domínio. Para obter mais informações sobre como pesquisar um domínio, consulte [Pesquisando conteúdo de domínio.](searching-domain-contents.md)

## <a name="searching-the-schema-container"></a>Pesquisando o contêiner de esquema

O contêiner de esquema contém os [**objetos classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que fornecem a definição formal de cada classe e atributo que podem existir no Active Directory Domain Services. Para pesquisar objetos no contêiner de esquema, a bind ao contêiner de esquema em qualquer controlador de domínio. O contêiner de esquema está disponível em todos os controladores de domínio. O nome diferenciado do contêiner de esquema é obtido do atributo **schemaNamingContext** de rootDSE. Para obter mais informações sobre rootDSE e o atributo **schemaNamingContext,** consulte Associação sem servidor [e RootDSE](serverless-binding-and-rootdse.md).

Para obter mais informações sobre a leitura do esquema ou do contêiner de esquema abstrato, consulte [Diretrizes](guidelines-for-binding-to-the-schema.md)para associação ao esquema .

## <a name="searching-the-configuration-container"></a>Pesquisando o contêiner de configuração

O contêiner de configuração contém informações de configuração, como sites, serviços e especificadores de exibição, para toda a floresta. Para pesquisar objetos no contêiner de configuração, a bind ao contêiner de configuração em qualquer controlador de domínio. O contêiner de configuração está disponível em todos os controladores de domínio. O nome diferenciado do contêiner de configuração é obtido do atributo **configurationNamingContext** de rootDSE. Para obter mais informações sobre rootDSE e o **atributo configurationNamingContext,** consulte Associação sem servidor [e RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Pesquisando o catálogo global

O catálogo global contém uma réplica de cada objeto Active Directory Domain Services, mas com apenas um pequeno número de seus atributos. Os atributos no catálogo global são aqueles usados com mais frequência em operações de pesquisa, como nome e sobrenome de um usuário, nomes de logon e assim por diante. Para obter mais informações sobre como pesquisar o catálogo global, consulte [Pesquisando o Catálogo Global.](searching-global-catalog-contents.md)

 

 