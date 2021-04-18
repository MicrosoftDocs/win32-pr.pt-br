---
description: As convenções de texto SNMP são mapeadas para tipos definidos pelo CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro de Convenção TEXTUAL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764456"
---
# <a name="textual-convention-macro"></a>Macro de Convenção TEXTUAL

As convenções de texto SNMP são mapeadas para tipos definidos pelo CIM.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

As regras de mapeamento a seguir se aplicam às convenções de texto SNMP:

-   A definição de tipo nomeado na cláusula SYNTAX mapeia literalmente para a **\_ sintaxe de objeto** de qualificador de propriedade CIM.
-   Use a tabela a seguir para mapear as convenções de texto quando a cláusula SYNTAX se referir explicitamente a uma convenção textual de uma macro de Convenção TEXTUAL do SNMPv2C ou se referir a uma convenção textual implícita. O valor padrão é sempre **nulo**.



| Convenção textual | Tipo de variante CIM | Qualificador CIM                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **\_ Convenção textual**: DateAndTime<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: DateAndTime<br/> **CimType**: cadeia de caracteres<br/>       |
| DisplayString      | **VT \_ BSTR**     | **\_ Convenção textual**: DisplayString<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: DisplayString<br/> **CimType**: cadeia de caracteres<br/>   |
| MacAddress         | **VT \_ BSTR**     | **\_ Convenção textual**: MACAddress<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: MACAddress<br/> **CimType**: cadeia de caracteres<br/>         |
| PhysAddress        | **VT \_ BSTR**     | **\_ Convenção textual**: PhysAddress<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: PhysAddress<br/> **CimType**: cadeia de caracteres<br/>       |
| SnmpUDPAddress     | **VT \_ BSTR**     | **\_ Convenção textual**: SnmpUDPAddress<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: SnmpUDPAddress<br/> **CimType**: cadeia de caracteres<br/> |
| SnmpOSIAddress     | **VT \_ BSTR**     | **\_ Convenção textual**: SnmpOSIAddress<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: SnmpOSIAddress<br/> **CimType**: cadeia de caracteres<br/> |
| SnmpIPXAddress     | **VT \_ BSTR**     | **\_ Convenção textual**: SnmpIPXAddress<br/> **codificação**: octetstring<br/> **\_ sintaxe do objeto**: SnmpIPXAddress<br/> **CimType**: cadeia de caracteres<br/> |



 

-   O tipo de variante definido pelo CIM e os qualificadores de propriedade CIM **\_ Convenção textual**, **codificação**, **\_ sintaxe de objeto** e mapa **CimType** usando o tipo primitivo subjacente.
-   A cláusula DISPLAY-HINT da macro de Convenção TEXTUAL do SNMPv2C mapeia textualmente para a dica de **exibição \_** do qualificador de propriedade CIM. Esse qualificador não será gerado se não houver uma macro de Convenção TEXTUAL ou a macro não contiver uma cláusula de dica de exibição.

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir descreve uma Convenção de texto SNMPv1.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

Este exemplo gera os seguintes qualificadores CIM.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

O exemplo a seguir descreve uma convenção textual de SNMPv2.

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

Este exemplo gera os seguintes qualificadores CIM.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




