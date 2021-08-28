---
description: Descreve os erros de provedor WMI SNMP de 1011 a 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Erros de 1011 a 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49642dd17180b32a683ec7937553dbe60c60584e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886981"
---
# <a name="errors-1011-through-1020"></a>Erros de 1011 a 1020

Descreve os erros de provedor WMI SNMP de 1011 a 1020.

[Erro fatal 1011](#fatal-error-1011)

[Erro fatal 1012](#fatal-error-1012)

[Erro fatal 1013](#fatal-error-1013)

[Aviso 1014](#warning-1014)

[Erro fatal 1015](#fatal-error-1015)

[Erro fatal 1016](#fatal-error-1016)

[Erro fatal 1018](#fatal-error-1018)

[Erro fatal 1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>Erro fatal 1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Fatal>: " fileName :<line> a SINTAXE do identificador de membro sequence, identifier , difere da cláusula SYNTAX do &lt; &gt; \# &lt; &gt; &lt; &gt; OBJECT-TYPE"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. Um elemento de uma SEQUENCE deve ser igual ao tipo na cláusula SYNTAX da definição OBJECT-TYPE. O <linha> parâmetro é a linha da \# cláusula SYNTAX da definição OBJECT-TYPE.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1012"></a>Erro fatal 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Fatal>: " fileName :<line> Uma cláusula INDEX ou AUGMENTS é necessária apenas para &lt; &gt; SEQUENCE \# OBJECT-TYPES"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. Uma cláusula INDEX só deve estar presente em uma definição OBJECT-TYPE cuja SINTAXE é resolvida para um tipo SEQUENCE.

Esse erro pode ocorrer ao compilar um MIB SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1013"></a>Erro fatal 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Fatal>: " &lt; fileName &gt;<line \#>: &lt; identifier should resolve to a SEQUENCE &gt; type"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. Um tipo usado no constructo "SEQUENCE OF" deve ser resolvido para um tipo SEQUENCE.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="warning-1014"></a>Aviso 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Aviso>: " &lt; fileName :<line>: Sub-identifier do valor 0 não recomendado em &gt; \# OIDs"**
</dt> <dd>

**Aviso semântico do** módulo de invocação de macro OBJECT-TYPE. É recomendável que nenhum objeto em um Internet Standard MIB use um sub identificador de zero em seu IDENTIFICADOR DE OBJETO.

Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1015"></a>Erro fatal 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Fatal>: " &lt; fileName &gt; :<line \#>: OBJECT-TYPEs &lt; identifier from module identifier and &gt; &lt; identifier from module identifier aresigned &gt; &lt; the same &gt; &lt; &gt; OID values"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. Duas **invocações OBJECT-TYPE** (nos mesmos módulos ou módulos diferentes) não devem ser atribuídas ao mesmo valor do Identificador de Objeto.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1016"></a>Erro fatal 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Fatal>: " &lt; fileName &gt; :<line>: Value in the DEFVAL clause does not match the type in \# the SYNTAX clause"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. Um valor em uma cláusula DEFVAL deve ser um valor do tipo mencionado na cláusula SYNTAX.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1018"></a>Erro fatal 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Fatal>: " fileName<line>: o símbolo na cláusula ENTERPRISE de TRAP-TYPE não é resolvido para um &lt; &gt; valor \# &lt; &gt; OID"**
</dt> <dd>

**Invocação de macro TRAP-TYPE,** erro semântico de módulo específico de SNMPv1. O símbolo usado na cláusula ENTERPRISE de uma invocação de macro **TRAP-TYPE** deve ser resolvido para um valor do Identificador de Objeto.

</dd> </dl>

## <a name="fatal-error-1020"></a>Erro fatal 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, fatal>: " fileName<line>: o valor atribuído ao &lt; &gt; \# identificador TRAP-TYPE não resolve para um inteiro &lt; &gt; positivo"**
</dt> <dd>

**Invocação de macro TRAP-TYPE,** erro semântico de módulo específico de SNMPv1. Um símbolo usado na especificação do valor de interceptação não é resolvido para um inteiro positivo.

</dd> </dl>

 

 



