---
description: Especifica uma chave para selecionar uma linha exclusiva em uma coleção escalar ou de tabela.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: Cláusula INDEX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca4478164839412238f59d9771aa9c96417c4055390cb4599edbb40b0e6b4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318738"
---
# <a name="index-clause"></a>Cláusula INDEX

A cláusula INDEX especifica uma chave para selecionar uma linha exclusiva em uma coleção escalar ou de tabela. O Provedor SNMP é mapeado para um tipo diferente de classe CIM, dependendo do tipo de tabela que o dispositivo SNMP usa. Como uma chave pode ser mais de um tipo de objeto, o provedor usa regras de mapeamento diferentes, dependendo do tipo de objeto dentro da chave. Para obter mais informações, consulte [Tipos de dados da cláusula INDEX](#index-clause-data-types).

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Uma coleção escalar mapeia para uma classe singleton CIM: ou seja, uma classe que pode ter apenas uma instância. Como não há necessidade de identificar exclusivamente uma instância de outra, uma classe singleton não designa uma ou mais propriedades como a chave. Classes geradas de coleções escalares:

-   Não contêm **qualificadores de** propriedade Key.
-   Contêm o singleton do qualificador de classe CIM **padrão,** que é do tipo **Bool.**

Uma coleção de tabelas mapeia para uma classe CIM que pode ter mais de uma instância. Como resultado, a definição da classe CIM deve conter pelo menos uma propriedade que define a chave de objeto; ou seja, uma propriedade que identifica exclusivamente uma instância da classe . A cláusula INDEX da macro [OBJECT-TYPE](object-type-macro.md) de uma coleção de tabela especifica o conjunto de propriedades de chave da coleção. As seguintes regras de mapeamento se aplicam:

-   A chave do **qualificador** CIM, tipo **Bool,** define uma propriedade de chave.
-   A ordenação das informações INDEX na coleção de tabelas define a ordenação das chaves dentro da definição da classe CIM.

    A Ordem de Chave do **qualificador \_** CIM define a ordenação das chaves. Esse qualificador é um valor inteiro de 32 bits sem sinal que, para fins da sintaxe do qualificador MOF, deve ser convertido em um valor inteiro de 32 bits assinado usando a operação twos-complement.

Atualmente, o mapeamento da cláusula SNMPv2C INDEX não lida com o uso do qualificador **IMPLÍCITO.** Uma definição de classe CIM não é gerada nesse caso.

## <a name="index-clause-data-types"></a>Tipos de dados da cláusula INDEX

Devido à flexibilidade da cláusula INDEX dentro da macro [OBJECT-TYPE,](object-type-macro.md) a especificação das propriedades com chave não é simples. Em vez disso, você deve considerar as possibilidades de que a cláusula INDEX possa conter um ou mais dos seguintes tipos de dados:

-   Valor **indexobject acessível** internamente

    O **valor indexobject** é um valor nomeado que se refere a uma definição de objeto MIB que aparece na linha conceitual da mesma tabela que contém a cláusula INDEX. A definição de objeto MIB referenciada na cláusula INDEX é mapeada para uma propriedade de chave da definição da classe CIM.

-   Valor **indexobject acessível externamente**

    Nesse caso, **indexobject** é um valor nomeado que se refere a uma definição de objeto MIB que aparece na linha conceitual de uma tabela diferente.

-   Valor **de indextype acessível**

    O **valor indextype** é um tipo nomeado que se refere a um dos seguintes tipos de dados: **INTEGER**, **OCTET STRING**, OBJECT **IDENTIFIER,** **NetworkAddress** ou **IpAddress**. Se a cláusula INDEX contiver uma referência do tipo MIB, as seguintes regras de mapeamento se aplicarão:

    -   O objeto MIB referenciado é mapeado para uma propriedade de chave da definição da classe CIM. Sua sintaxe de tipo é baseada no valor **indextype** especificado, que mapeia para qualificadores de propriedade CIM usando os procedimentos de mapeamento de [cláusula SYNTAX](syntax-clause.md) padrão.
    -   O processo de mapeamento gera um nome de propriedade exclusivo concatenando o descritor de objeto da tabela MIB, um sublinhado ( ) e a ordem de classificação do valor indextype da cláusula \_ INDEX.  Por exemplo, o nome da propriedade para o terceiro tipo de **índice de** componente da tabela MIB **enterpriseIfTable** é **enterpriseIfTable \_ 3**.
    -   A propriedade CIM é anotada com o **qualificador \_ de Chave Virtual.** Esse qualificador especifica que o Provedor SNMP deve calcular o valor da propriedade com base no superconjunto de informações de instância associadas a todas as definições de objeto MIB acessíveis na definição de classe.
    -   A definição da classe CIM deve conter pelo menos uma propriedade que não tenha um qualificador de Chave **Virtual \_** associado; a falha ao especificar essa propriedade invalida a definição de classe.

-   Subtipo de comprimento fixo

    Quando a cláusula INDEX de uma coleção de tabelas SNMP contém um tipo com suporte de SNMP que é subtipo como uma CADEIA DE CARACTERES OCTET de comprimento fixo, o comprimento fixo do **qualificador \_** de propriedade CIM deve ser usado para especificar esse valor.

 

 



