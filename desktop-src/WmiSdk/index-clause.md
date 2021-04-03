---
description: Especifica uma chave para selecionar uma linha exclusiva em uma coleção escalar ou de tabela.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: Cláusula de índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cbe1c4bf1da5ccd7fbab881770722b70bc53c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091757"
---
# <a name="index-clause"></a>Cláusula de índice

A cláusula INDEX especifica uma chave para selecionar uma linha exclusiva em uma coleção escalar ou de tabela. O provedor SNMP é mapeado para um tipo diferente de classe CIM dependendo do tipo de tabela que o dispositivo SNMP usa. Como uma chave pode ser mais de um tipo de objeto, o provedor usa diferentes regras de mapeamento dependendo do tipo de objeto dentro da chave. Para obter mais informações, consulte [tipos de dados de cláusula de índice](#index-clause-data-types).

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Uma coleção escalar é mapeada para uma classe singleton do CIM: ou seja, uma classe que pode ter apenas uma instância. Como não há necessidade de identificar exclusivamente uma instância de outra, uma classe singleton não designa uma ou mais propriedades como a chave. Classes geradas a partir de coleções escalares:

-   Não contêm qualificadores de propriedade de **chave** .
-   Contém o **singleton** de qualificador de classe CIM padrão, que é do tipo **bool**.

Uma coleção de tabelas é mapeada para uma classe CIM que pode ter mais de uma instância. Como resultado, a definição da classe CIM deve conter pelo menos uma propriedade que define a chave do objeto; ou seja, uma propriedade que identifica exclusivamente uma instância da classe. A cláusula INDEX da macro do tipo de [objeto](object-type-macro.md) de uma coleção de tabelas especifica o conjunto de propriedades de chave da coleção. As seguintes regras de mapeamento se aplicam:

-   A **chave** do qualificador CIM, tipo **bool**, define uma propriedade de chave.
-   A ordenação das informações de índice na coleção de tabelas define a ordenação das chaves dentro da definição da classe CIM.

    A ordem da **chave \_** do qualificador CIM define a ordenação das chaves. Esse qualificador é um valor inteiro de 32 bits sem sinal, que, para os fins da sintaxe do qualificador MOF, deve ser convertido em um valor inteiro de bit 32 assinado usando a operação dois Complementos-complemento.

Atualmente, o mapeamento da cláusula de índice do SNMPv2C não manipula o uso do qualificador **implícito** . Uma definição de classe CIM não é gerada nesse caso.

## <a name="index-clause-data-types"></a>Tipos de dados de cláusula de índice

Devido à flexibilidade da cláusula INDEX dentro da macro do [tipo Object](object-type-macro.md) , a especificação das propriedades com chave não é simples. Em vez disso, você deve considerar as possibilidades que a cláusula INDEX pode conter um ou mais dos seguintes tipos de dados:

-   Valor de **IndexObject** acessível internamente

    O valor de **IndexObject** é um valor nomeado que se refere a uma definição de objeto MIB que aparece na linha conceitual da mesma tabela que contém a cláusula index. A definição do objeto MIB referenciada na cláusula INDEX é mapeada para uma propriedade Key da definição da classe CIM.

-   Valor **IndexObject** acessível externamente

    Nesse caso, **IndexObject** é um valor nomeado que se refere a uma definição de objeto MIB que aparece na linha conceitual de uma tabela diferente.

-   Valor de **indextype** acessível

    O valor de **indextype** é um tipo nomeado que se refere a um dos seguintes tipos de dados: **inteiro**, **cadeia de caracteres de octeto**, identificador de **objeto**, **networkaddress** ou **IPAddress**. Se a cláusula INDEX contiver uma referência de tipo MIB, as seguintes regras de mapeamento se aplicarão:

    -   O objeto MIB referenciado mapeia para uma propriedade de chave da definição de classe CIM. Sua sintaxe de tipo se baseia no valor de **indextype** especificado, que é mapeado para qualificadores de propriedade CIM usando os procedimentos de mapeamento de [cláusula de sintaxe](syntax-clause.md) padrão.
    -   O processo de mapeamento gera um nome de propriedade exclusivo concatenando o descritor de objeto da tabela MIB, um sublinhado ( \_ ) e a ordem de classificação do valor **indextype** da cláusula index. Por exemplo, o nome da propriedade para o terceiro **indextype** do componente da tabela MIB **enterpriseIfTable** é **enterpriseIfTable \_ 3**.
    -   A propriedade CIM é anotada com o qualificador de **\_ chave virtual** . Esse qualificador especifica que o provedor SNMP deve calcular o valor da propriedade com base no superconjunto das informações de instância associadas a todas as definições de objeto MIB acessíveis na definição de classe.
    -   A definição da classe CIM deve conter pelo menos uma propriedade que não tenha um qualificador de **\_ chave virtual** associado; a falha ao especificar essa propriedade invalida a definição de classe.

-   Subtipo de comprimento fixo

    Quando a cláusula de índice de uma coleção de tabelas SNMP contém um tipo com suporte de SNMP que é subtipoado como uma cadeia de caracteres de OCTETO de comprimento fixo, o **\_ comprimento fixo** do qualificador de propriedade CIM deve ser usado para especificar esse valor.

 

 



