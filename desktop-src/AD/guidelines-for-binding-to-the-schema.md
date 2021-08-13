---
title: Diretrizes para associação ao esquema
description: Há duas maneiras de se associar ao esquema de Active Directory associar diretamente ao contêiner de esquema ou a um objeto classSchema ou attributeSchema no contêiner de esquema.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Diretrizes para associação ao AD do esquema
- AD Schema, ligando para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1492814bbce4b359a16c10f1d92340ae06d0f3c58177cd125a0b0c861f32f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188680"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Diretrizes para associação ao esquema

Há duas maneiras de se associar ao esquema de Active Directory:

-   Associe diretamente ao contêiner de esquema ou a um objeto **classSchema** ou **attributeSchema** no contêiner de esquema. Os objetos **classSchema** ou **attributeSchema** contêm definições completas e formais de cada classe e atributo que podem existir em uma floresta domínio do Active Directory. Para obter mais informações, consulte [lendo objetos attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).
-   Associe-se ao esquema abstrato ou a uma entrada de classe ou atributo no esquema abstrato. O esquema abstrato contém apenas um subconjunto dos dados sobre cada classe e atributo, mas os dados estão em um formato fácil de recuperar e usar. Para obter mais informações, consulte [o esquema abstrato](the-abstract-schema.md) e [lendo o esquema abstrato](reading-the-abstract-schema.md).

Para modificar ou estender o esquema, associe diretamente ao contêiner de esquema. Para ler as definições de classe e de atributo, geralmente é mais fácil ler do esquema abstrato.

É mais fácil ler a partir do esquema abstrato pelos seguintes motivos:

-   A ADSI fornece técnicas de ligação especiais e um conjunto de interfaces para ler o esquema abstrato.
-   As interfaces ADSI que funcionam com o esquema abstrato retornam dados em um formato apropriado para uso em outras interfaces ADSI. Por exemplo, [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) e [**iadsproperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) normalmente usam cadeias de caracteres **lDAPDisplayName** para relatar nomes de atributo e de classe, embora esses dados sejam armazenados no diretório na forma de OIDs (identificadores de objeto). O formato **lDAPDisplayName** é conveniente porque outras interfaces ADSI o utilizam para fazer referência a classes e atributos em filtros de pesquisa e em outro lugar.
-   A entrada de esquema abstrata para uma classe de objeto contém dados coletados de vários objetos **classSchema** . Por exemplo, os possíveis pais, atributos obrigatórios e atributos opcionais para uma classe de objeto são a União desses atributos das superclasses e das classes auxiliares da classe. Se você ler o contêiner de esquema real, precisará coletar dados de vários objetos **classSchema** dos quais a classe foi derivada. Se você ler o esquema abstrato, os dados ficarão em um único lugar.

Você deve associar diretamente ao contêiner de esquema em vez de usar o esquema abstrato nos seguintes casos:

-   Para obter atributos específicos não expostos no esquema abstrato. Por exemplo, **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** e outros atributos não são expostos no esquema abstrato.
-   Para consultar objetos **attributeSchema** e **classSchema** . Para pesquisar classes ou atributos que correspondam a um filtro especificado, associe-se ao contêiner de esquema e execute uma pesquisa de nível único.
-   Para adicionar ou modificar atributos ou classes. O esquema abstrato é somente leitura; Você não pode usá-lo para modificar ou estender o esquema. Lembre-se de que as modificações devem ser feitas no controlador de domínio que é o mestre de esquema. Para obter mais informações, consulte [pré-requisitos para instalar uma extensão de esquema](prerequisites-for-installing-a-schema-extension.md).

 

 