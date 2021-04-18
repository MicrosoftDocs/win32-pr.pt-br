---
description: Descreve os erros do provedor SNMP WMI 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Erros 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793951"
---
# <a name="errors-1001-through-1010"></a>Erros 1001 a 1010

Descreve os erros do provedor SNMP WMI 1001 a 1010.

[Erro fatal 1001](#fatal-error-1001)

[Erro fatal 1002](#fatal-error-1002)

[Erro fatal 1003](#fatal-error-1003)

[Aviso 1004](#warning-1004)

[Aviso 1005](#warning-1005)

[Erro fatal 1006](#fatal-error-1006)

[Erro fatal 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Erro fatal 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, fatal>: " <fileName> : <linha \#>: a cláusula Syntax do tipo Object não é resolvida para tipos permitidos"
</dt> <dd>

Erro semântico do módulo de invocação de macro do tipo de objeto. A cláusula de sintaxe da macro do tipo de objeto deve ser resolvida para um tipo ou subtipo, formado usando a especificação de tamanho ou intervalo que o SMI ou de SNMPv2C permite. Se esse não for o caso, o erro fatal 1001 será relatado.

Esse erro pode ocorrer durante a compilação de uma MIB ou do SNMPv2C.

Os tipos permitidos pelo SMI do SNMPv1 são:

-   INTEGER
-   NULO
-   CADEIA DE CARACTERES DE OCTETO
-   IDENTIFICADOR DE OBJETO
-   NetworkAddress
-   IpAddress
-   Contador
-   Medidor
-   TimeTicks
-   Opaco
-   DisplayString
-   PhysAddress

Os tipos permitidos pelo SMI do SNMPv2C são:

-   INTEGER
-   CADEIA DE CARACTERES DE OCTETO
-   IDENTIFICADOR DE OBJETO
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   TimeTicks
-   Opaco
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   Verdadevalue
-   TestAndIncr
-   Autônomo
-   InstancePointer
-   VariablePointer
-   Ponto de extremidade
-   UserStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Taddress

</dd> </dl>

## <a name="fatal-error-1002"></a>Erro fatal 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> fatal: " <fileName> : <linha \#>: cláusula de acesso inválida <clause> "
</dt> <dd>

Erro semântico do módulo de invocação de macro do tipo de objeto. Para SNMPv1, a cláusula de acesso da macro do tipo de objeto deve ser "somente leitura", "somente gravação", "leitura/gravação" ou "não acessível".

Para o SNMPv2C, a cláusula MAX-ACCESS deve ser "somente leitura", "leitura-criação", "leitura/gravação" ou "não acessível".

</dd> </dl>

## <a name="fatal-error-1003"></a>Erro fatal 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> fatal: " <fileName> : <linha \#>: cláusula status inválida <clause> "
</dt> <dd>

Erro semântico do módulo de invocação de macro do tipo de objeto. Para SNMPv1, a cláusula STATUS de uma chamada de macro de tipo de objeto deve ser "obrigatória", "opcional," "obsoleto" ou "preterido".

Para o SNMPv2C, a cláusula STATUS de uma chamada de macro de tipo de objeto deve ser "Current", "preterido" ou "obsoleto".

</dd> </dl>

## <a name="warning-1004"></a>Aviso 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, aviso>: " <fileName> : <linha \#>: tipo de objeto <identifier> , cuja sintaxe resolve para um dos tipos de contadores não termina com a letra '"
</dt> <dd>

Aviso semântico do módulo de invocação de macro do tipo de objeto. O identificador de um objeto do contador de sintaxe (SNMPv1) ou Counter32 e Counter64 (SNMPv2C) deve ser plural.

Esse aviso pode ocorrer durante a compilação de uma MIB ou do SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>Aviso 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, aviso>: " <fileName> : <linha \#>: tipo de objeto com sintaxe" Sequence of ", deve ter uma cláusula de acesso" não acessível "
</dt> <dd>

Aviso semântico do módulo de invocação de macro do tipo de objeto. Uma tabela ou linha conceitual (sequência ou tipos de objetos de sequência, respectivamente) deve ser "não acessível".

Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Erro fatal 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, fatal>: " <fileName> : linha \# de <> tipo de objeto <identifier> , que é da sequência de sintaxe, não tem um índice ou uma cláusula de aumentos"
</dt> <dd>

Erro semântico do módulo de invocação de macro do tipo de objeto. Para SNMPv1, a cláusula INDEX deve estar presente para uma definição de tipo de objeto cuja sintaxe seja resolvida para um tipo de sequência.

Para o SNMPv2C, a cláusula de índice ou de AUMENTOs deve estar presente para uma declaração de linha conceitual.

</dd> </dl>

## <a name="fatal-error-1008"></a>Erro fatal 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, fatal>: " <fileName> : <linha \#>: tipo de objeto <identifier> , que é da sintaxe" Sequence "não foi referenciada"
</dt> <dd>

Erro semântico do módulo de invocação de macro do tipo de objeto. Um tipo de objeto com a cláusula SYNTAX como um tipo de sequência deve ser exibido na cláusula SYNTAX de exatamente uma invocação de tipo de objeto que significa uma declaração de tabela, ou seja, um objeto com a cláusula SYNTAX como uma sequência do tipo. O parâmetro de> de linha de <\# refere-se ao segundo ponto de referência.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

 

 



