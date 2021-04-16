---
description: Contém uma cláusula de sintaxe que define os dados e o tipo para o objeto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Cláusula de sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765229"
---
# <a name="syntax-clause"></a>Cláusula de sintaxe

A macro do [tipo de objeto](object-type-macro.md) contém uma cláusula de sintaxe que define os dados e o tipo do objeto MIB. Embora o provedor SNMP Observe as regras gerais para mapear cláusulas de sintaxe, o provedor também segue regras específicas para vários tipos de dados.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

As regras de mapeamento a seguir se aplicam a todos os tipos de dados descritos na tabela a seguir:

-   A representação textual da cláusula de sintaxe é mapeada para a **\_ Convenção textual** do qualificador de propriedade CIM.
-   A definição de tipo nomeado na cláusula SYNTAX é mapeada para a sintaxe de **objeto \_** de qualificador de propriedade CIM. Esse mapeamento difere dependendo do tipo de dados. Para obter mais informações, consulte as descrições de mapeamento.
-   O tipo SNMP usado ao codificar quadros de protocolo SNMPv1 e SNMPv2C é mapeado para a **codificação** qualificador de propriedade CIM.
-   O qualificador de propriedade CIM **CimType** contém a representação textual que formata o valor de protocolo CIM subjacente.

A tabela a seguir lista os tipos de dados que têm regras específicas que regem o comportamento de mapeamento do provedor.



| Tipo de dados SNMP                                     | Descrição                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo primitivo](#primitive-type)                  | Um dos tipos de dados básicos definidos na estrutura das informações de gerenciamento (SMI) documenta RFC 1213 e RFC 1903.                                                                                                                            |
| [Convenção textual](textual-convention-macro.md) | Definição de tipo gerada por meio do uso explícito da macro de **Convenção textual** do SNMPv2c ou gerada por meio do uso de um tipo nomeado. Uma convenção textual atribui um nome e, em alguns casos, um intervalo de valores a um tipo de dados existente. |
| [Tipo nomeado](#named-type)                          | Referência nomeada para um tipo primitivo, Convenção textual ou tipo restrito.                                                                                                                                                                    |
| [Tipo restrito](#constrained-type)              | Tipo primitivo, tipo nomeado ou convenção de texto que foi restringido por algum mecanismo de subdigitação definido nos documentos do SMI RFC 1213 e RFC 1903.                                                                                      |



 

## <a name="primitive-type"></a>Tipo primitivo

O tipo primitivo é um dos tipos de dados básicos definidos na estrutura de informações de gerenciamento (SMI) documentos RFC 1213 e RFC 1903. Os tipos primitivos SNMP são mapeados para tipos definidos pelo CIM. A tabela a seguir lista o mapeamento que ocorre quando a cláusula SYNTAX se refere explicitamente a um tipo primitivo para SNMPv1. Os qualificadores de **\_ sintaxe de objeto** , **codificação** e **\_ Convenção textual** são sempre iguais aos do tipo MIB e o valor padrão é sempre **nulo**.



| Tipo de MIB         | Tipo de variante CIM | valor de CimType |
|------------------|------------------|---------------|
| INTEGER          | \_I4 VT           | **sint32**    |
| OCTETstring      | VT \_ BSTR         | **cadeia de caracteres**    |
| OBJECTIDENTIFIER | VT \_ BSTR         | **cadeia de caracteres**    |
| NULO             | VT \_ nulo         | Sem suporte |
| IpAddress        | VT \_ BSTR         | **cadeia de caracteres**    |
| Contador          | \_I4 VT           | **uint32**    |
| Medidor            | \_I4 VT           | **uint32**    |
| TimeTicks        | \_I4 VT           | **uint32**    |
| Opaco           | VT \_ BSTR         | **cadeia de caracteres**    |
| NetworkAddress   | VT \_ BSTR         | **cadeia de caracteres**    |



 

O provedor ignora a macro do tipo de objeto quando a cláusula SYNTAX refere-se a **NULL**, seja explicitamente ou por meio de uma atribuição de tipo nomeado. A tabela a seguir lista o mapeamento que ocorre quando a cláusula SYNTAX se refere explicitamente a um tipo primitivo para SNMPv2. Os qualificadores de **\_ sintaxe de objeto** , **codificação** e **\_ Convenção textual** são sempre iguais aos do tipo MIB e o valor padrão é sempre **nulo**.



| Tipo de MIB          | Tipo de variante CIM | valor de CimType |
|-------------------|------------------|---------------|
| INTEGER           | \_I4 VT           | **sint32**    |
| CADEIA DE CARACTERES DE OCTETO      | VT \_ BSTR         | **cadeia de caracteres**    |
| IDENTIFICADOR DE OBJETO | VT \_ BSTR         | **cadeia de caracteres**    |
| IpAddress         | VT \_ BSTR         | **cadeia de caracteres**    |
| Counter32         | \_I4 VT           | **uint32**    |
| Gauge32           | \_I4 VT           | **uint32**    |
| Unsigned32        | \_I4 VT           | **uint32**    |
| Integer32         | \_I4 VT           | **sint32**    |
| Counter64         | VT \_ BSTR         | **uint64**    |
| TimeTicks         | \_I4 VT           | **uint32**    |
| Opaco            | VT \_ BSTR         | **cadeia de caracteres**    |



 

## <a name="named-type"></a>Tipo nomeado

Os tipos nomeados do SNMP são mapeados para tipos definidos pelo CIM. Quando a cláusula SYNTAX se refere a um [tipo primitivo](#primitive-type), [Convenção textual](textual-convention-macro.md)ou [tipo restrito](#constrained-type) por meio de uma derivação de atribuição de tipo, use esses tipos para determinar quais procedimentos de mapeamento se aplicam.

-   Se, por meio da derivação das regras de atribuição de tipo, você encontrará uma definição de tipo restrito:

    -   E se, por meio de derivação adicional, você encontrar uma das convenções textuais listadas na [macro de Convenção textual](textual-convention-macro.md), aplique as regras de mapeamento para tipos restritos e convenções de texto.
    -   Caso contrário, se você encontrar um dos tipos primitivos listados em uma tabela de tipo primitivo, aplique as regras de mapeamento para tipos primitivos e tipos restritos.

-   Se você encontrar uma das convenções textuais listadas na [ \_ macro Convenção textual](textual-convention-macro.md), aplique as regras de mapeamento para as convenções textuais.
-   Se você encontrar um dos tipos primitivos listados em uma tabela de tipo primitivo, aplique as regras de mapeamento para tipos primitivos.

> [!Note]  
> Classes que contêm tipos de propriedade que não estão em conformidade com o mapeamento descrito acima não são válidas. Nesse caso, o provedor retornará um erro se e quando o provedor solicitar a recuperação de uma definição de classe durante a execução de uma função de recuperação de instância.

 

## <a name="constrained-type"></a>Tipo restrito

Um tipo restrito é um tipo primitivo, tipo nomeado ou convenção textual que foi restringido por algum mecanismo de subdigitação definido nos documentos do SMI RFC 1213 e RFC 1903. Quando ocorre uma subdigitação, qualificadores CIM adicionais são necessários para especificar os valores de subtipo. A definição de tipo nomeado na cláusula de sintaxe mapeia literalmente para a **\_ sintaxe de objeto** do qualificador de propriedade CIM até, mas não incluindo as restrições do subtipo.

Os subtipos podem seguir qualquer um dos seguintes formatos:

-   INTEIRO enumerado

    A **Enumeração** de qualificador de propriedade CIM especifica os valores enumerados. Esse qualificador é representado como uma cadeia de caracteres que contém uma lista separada por vírgulas de valores inteiros de 32 bits assinados. A tabela a seguir lista os tipos de mapeamento. O valor padrão é sempre **nulo**.



| Tipo de MIB restrito | Tipo de variante CIM | Qualificadores CIM                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| INTEIRO enumerado   | VT \_ BSTR         | **\_ Convenção textual**: enumeratedinteger<br/> **codificação**: inteiro<br/> **CimType**: cadeia de caracteres<br/> |



 

-   BITS

    Os **bits** do qualificador de propriedade CIM especificam os valores enumerados. Esse qualificador é representado como uma cadeia de caracteres que contém uma lista separada por vírgulas de valores inteiros de 32 bits assinados. A tabela a seguir lista os tipos de mapeamento. O valor padrão é sempre **nulo**.



| Tipo de MIB restrito | Tipo de variante CIM      | Qualificadores CIM                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | \_matriz VT \| VT \_ BSTR | **\_ Convenção textual**: bits<br/> **codificação**: octetstring<br/> **CimType**: cadeia de caracteres<br/> |



 

-   Comprimento variável

    Quando a cláusula SYNTAX refere-se a um tipo primitivo, tipo nomeado ou convenção textual que é subtipoada como uma cadeia de caracteres de OCTETO de comprimento variável ou opaco, **o \_ comprimento da variável** de qualificador de propriedade CIM especifica os valores mínimo, máximo e de comprimento fixo associados à definição de tipo. Esse qualificador é implementado como uma cadeia de caracteres no seguinte formato em que os valores de comprimento variável são representados como inteiros de 32 bits sem sinal.

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   Comprimento fixo

    Quando a cláusula SYNTAX refere-se a um tipo primitivo, tipo nomeado ou convenção textual que é subtipoado como uma cadeia de caracteres de OCTETO de comprimento fixo ou opaco, **o \_ comprimento fixo** do qualificador de propriedade CIM especifica o valor de comprimento fixo. Esse qualificador é representado como um valor inteiro de 32 bits sem sinal.

-   Intervalo

    Quando a cláusula SYNTAX refere-se a um tipo primitivo, um tipo nomeado ou uma convenção textual que é subtipoda como um inteiro ou medidor de valor fixo ou de intervalo, o **\_ valor da variável** qualificador de propriedade CIM especifica os valores de intervalo e fixo associados à definição de tipo. Esse qualificador é implementado como uma cadeia de caracteres no seguinte formato em que os valores de intervalo e comprimento fixo são representados como inteiros de 32 bits sem sinal.

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir descreve um subtipo inteiro enumerado.

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

Este exemplo é mapeado para:

``` syntax
enumeration("up(1),down(2),testing(3)")
```

O exemplo de código a seguir descreve um subtipo BITS.

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

O exemplo de código a seguir mapeia para:

``` syntax
bits("up(1),down(2),testing(3)")
```

O exemplo de código a seguir descreve um subtipo de comprimento variável.

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

Este exemplo é mapeado para:

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

O exemplo a seguir descreve um subtipo de comprimento fixo.

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

Este exemplo é mapeado para:

``` syntax
fixed_length(6)
```

O exemplo a seguir descreve um subtipo de intervalo.

``` syntax
Status := INTEGER (10..20|8)
```

Este exemplo é mapeado para:

``` syntax
variable_value("10..20,8")
```

 

 




