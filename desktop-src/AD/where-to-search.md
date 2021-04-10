---
title: Decidindo onde Pesquisar
description: Este tópico explica as diferentes pesquisas que podem ser executadas no Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidindo onde Pesquisar o AD
- Active Directory AD, pesquisando, decidindo onde Pesquisar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293880"
---
# <a name="deciding-where-to-search"></a>Decidindo onde Pesquisar

Este tópico explica as diferentes pesquisas que podem ser executadas no Active Directory Domain Services.

Todas as pesquisas são executadas em um dos seguintes contextos de nomenclatura:

-   Domínio, incluindo partições de diretório de aplicativo
-   Contêiner de esquema
-   Contêiner de configuração
-   Catálogo global

## <a name="searching-a-domain"></a>Pesquisando um domínio

Os domínios contêm a maioria dos objetos altamente usados, como usuários, contatos, grupos, unidades organizacionais, computadores e assim por diante. A maioria das consultas pesquisará um domínio. Para obter mais informações sobre como pesquisar um domínio, consulte [pesquisando o conteúdo do domínio](searching-domain-contents.md).

## <a name="searching-the-schema-container"></a>Pesquisando o contêiner de esquema

O contêiner de esquema contém os objetos [**classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que fornecem a definição formal de todas as classes e atributos que podem existir em Active Directory Domain Services. Para pesquisar objetos no contêiner de esquema, associe-se ao contêiner de esquema em qualquer controlador de domínio. O contêiner de esquema está disponível em todos os controladores de domínio. O nome distinto do contêiner de esquema é obtido do atributo **schemaNamingContext** de RootDSE. Para obter mais informações sobre o rootDSE e o atributo **schemaNamingContext** , consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).

Para obter mais informações sobre a leitura do contêiner esquema ou esquema abstrato, consulte [diretrizes para associação ao esquema](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Pesquisando o contêiner de configuração

O contêiner de configuração contém informações de configuração, como sites, serviços e especificadores de exibição, para toda a floresta. Para pesquisar objetos no contêiner de configuração, associe-se ao contêiner de configuração em qualquer controlador de domínio. O contêiner de configuração está disponível em todos os controladores de domínio. O nome distinto do contêiner de configuração é obtido do atributo **configurationNamingContext** de RootDSE. Para obter mais informações sobre o rootDSE e o atributo **configurationNamingContext** , consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Pesquisando o catálogo global

O catálogo global mantém uma réplica de cada objeto em Active Directory Domain Services, mas com apenas um pequeno número de seus atributos. Os atributos no catálogo global são aqueles usados com mais frequência em operações de pesquisa, como nomes e sobrenome de um usuário, nomes de logon e assim por diante. Para obter mais informações sobre como pesquisar o catálogo global, consulte [pesquisando o catálogo global](searching-global-catalog-contents.md).

 

 