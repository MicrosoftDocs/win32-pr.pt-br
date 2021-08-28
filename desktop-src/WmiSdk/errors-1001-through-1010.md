---
description: Descreve os erros de provedor WMI SNMP de 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Erros de 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c754936d8900a16b89be1f1137984ee6e7d40
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886368"
---
# <a name="errors-1001-through-1010"></a>Erros de 1001 a 1010

Descreve os erros de provedor WMI SNMP de 1001 a 1010.

[Erro fatal 1001](#fatal-error-1001)

[Erro fatal 1002](#fatal-error-1002)

[Erro fatal 1003](#fatal-error-1003)

[Aviso 1004](#warning-1004)

[Aviso 1005](#warning-1005)

[Erro fatal 1006](#fatal-error-1006)

[Erro fatal 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Erro fatal 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: " &lt; fileName :<line>: a cláusula SYNTAX de OBJECT-TYPE não é resolvida para tipos &gt; \# permitidos"
</dt> <dd>

Erro semântico de módulo de invocação de macro OBJECT-TYPE. A cláusula SYNTAX da macro OBJECT-TYPE deve ser resolvida para um tipo ou subtipo, formado usando a especificação SIZE ou range que o SMI SNMPv1 ou SNMPv2C permite. Se esse não for o caso, o erro fatal 1001 será relatado.

Esse erro pode ocorrer ao compilar um MIB SNMPv1 ou SNMPv2C.

Os tipos permitidos pelo SMI SNMPv1 são:

-   INTEGER
-   NULO
-   CADEIA DE CARACTERES OCTETO
-   IDENTIFICADOR DE OBJETO
-   Networkaddress
-   IpAddress
-   Contador
-   Medidor
-   TimeTicks
-   Opaco
-   DisplayString
-   PhysAddress

Os tipos permitidos pelo SMI SNMPv2C são:

-   INTEGER
-   CADEIA DE CARACTERES OCTETO
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
-   TruthValue
-   TestAndIncr
-   AutonomousType
-   InstancePointer
-   VariablePointer
-   RowPointer
-   RowStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Dress

</dd> </dl>

## <a name="fatal-error-1002"></a>Erro fatal 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: " &lt; fileName &gt; :<line \#>: cláusula ACCESS &lt; inválida &gt; "
</dt> <dd>

Erro semântico de módulo de invocação de macro OBJECT-TYPE. Para SNMPv1, a cláusula ACCESS da macro OBJECT-TYPE deve ser "somente leitura", "somente gravação", "leitura/gravação" ou "não acessível".

Para SNMPv2C, a cláusula MAX-ACCESS deve ser "somente leitura", "read-create", "leitura/gravação" ou "não acessível".

</dd> </dl>

## <a name="fatal-error-1003"></a>Erro fatal 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: " &lt; fileName &gt; :<line \#>: cláusula STATUS inválida &lt; &gt; "
</dt> <dd>

Erro semântico de módulo de invocação de macro OBJECT-TYPE. Para SNMPv1, a cláusula STATUS de uma invocação de macro OBJECT-TYPE deve ser "obrigatória", "opcional", "obsoleta" ou "preterida".

Para SNMPv2C, a cláusula STATUS de uma invocação de macro OBJECT-TYPE deve ser "atual", "preterida" ou "obsoleta".

</dd> </dl>

## <a name="warning-1004"></a>Aviso 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Aviso>: " &lt; fileName &gt; :<line \#>: OBJECT-TYPE identifier , cuja sintaxe é resolvida para um dos tipos counter não termina com a letra &lt; &gt; 's' "
</dt> <dd>

Aviso semântico do módulo de invocação de macro OBJECT-TYPE. O identificador de um objeto de Contador DE SINTAXE (SNMPv1) ou Counter32 e Counter64 (SNMPv2C) deve ser plural.

Esse aviso pode ocorrer ao compilar um MIB SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>Aviso 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Aviso>: " &lt; fileName &gt; :<line \#>: OBJECT-TYPE com SINTAXE "SEQUENCE OF", deve ter uma cláusula ACCESS "não acessível"
</dt> <dd>

Aviso semântico do módulo de invocação de macro OBJECT-TYPE. Uma tabela ou linha conceitual (tipos de objeto SEQUENCE OF ou SEQUENCE, respectivamente) deve ser "não acessível".

Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Erro fatal 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: " &lt; fileName &gt; :<line \#> OBJECT-TYPE identifier , que é de SINTAXE SEQUENCE, não tem uma cláusula INDEX ou &lt; &gt; AUGMENTS"
</dt> <dd>

Erro semântico de módulo de invocação de macro OBJECT-TYPE. Para SNMPv1, a cláusula INDEX deve estar presente para uma definição OBJECT-TYPE cuja SINTAXE é resolvida para um tipo SEQUENCE.

Para SNMPv2C, a cláusula INDEX ou AUGMENTS deve estar presente para uma declaração de linha conceitual.

</dd> </dl>

## <a name="fatal-error-1008"></a>Erro fatal 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: " &lt; fileName &gt; :<line>: OBJECT-TYPE identifier , que é de SINTAXE "SEQUENCE" não foi \# &lt; &gt; referenciado"
</dt> <dd>

Erro semântico de módulo de invocação de macro OBJECT-TYPE. Um OBJECT-TYPE com a cláusula SYNTAX como um tipo SEQUENCE deve figurar na cláusula SYNTAX de exatamente uma invocação OBJECT-TYPE que representa uma declaração de tabela, ou seja, um objeto com a cláusula SYNTAX como um tipo SEQUENCE OF. O <linha \#> parâmetro refere-se ao segundo ponto de referência.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

 

 



