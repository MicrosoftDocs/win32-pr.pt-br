---
description: Uma coleção SNMP é mapeada para uma classe CIM e os elementos de uma coleção são mapeados para as propriedades de uma classe CIM. Todas as definições de classe CIM geradas devem ser derivadas da classe SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Coleções SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df4926ab89a6bb9a936fe5bdb27f921699bbe90a528842d81de96d8049412940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315300"
---
# <a name="snmp-collections"></a>Coleções SNMP

Uma coleção SNMP é mapeada para uma classe CIM e os elementos de uma coleção são mapeados para as propriedades de uma classe CIM. Todas as definições de classe CIM geradas devem ser derivadas da classe **SnmpObjectType** .

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

As seguintes definições de classe pai têm todas as definições de classe geradas:

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a>Comentários

As regras a seguir se aplicam ao mapear coleções SNMP para classes CIM. A menos que especificado de outra forma, essas regras se aplicam a coleções escalares e de tabela:

-   O processo de mapeamento gera nomes de classe CIM concatenando "SNMP \_ ", o nome de identidade do módulo MIB, " \_ " e o descritor de objeto da coleção.

    Por exemplo: o **sistema** se traduz no **\_ \_ \_ sistema MIB RFC1213 SNMP**, enquanto o **iftable** se traduz em **SNMP \_ RFC1213 \_ MIB \_ iftable**.

-   Em todos os casos, hifens (-) em identificadores de MIB SNMP são mapeados para sublinhados ( \_ ) em nomes de classe CIM.
-   Conflitos de nomenclatura podem ocorrer devido a uma não diferenciação de maiúsculas e minúsculas de nome CIM. Se ocorrer um conflito de nomenclatura, o provedor escolherá uma das definições de Grupo conflitantes e ignorará as definições restantes.
-   O nome de identidade do módulo MIB que contém a coleção é mapeado para o nome do **módulo \_** qualificador de classe CIM.
-   O identificador de objeto da coleção criei é mapeado para o ObjectID do **grupo \_** de qualificador de classe CIM.
-   A lista de importações do módulo MIB (obtida da definição de macro de **identidade de módulo** ) é mapeada para **as \_ importações do módulo** de qualificador de classe CIM. Esse qualificador contém uma lista separada por vírgulas de nomes de módulo.

 

 



