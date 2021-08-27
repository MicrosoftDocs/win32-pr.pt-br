---
description: Descreve os erros de provedor WMI SNMP de 1091 a 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Erros de 1091 a 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc57b8eb628de86b4a7d737bacec13bc2fdeadfb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880085"
---
# <a name="errors-1091-through-1100"></a>Erros de 1091 a 1100

Descreve os erros de provedor WMI SNMP de 1091 a 1100.

[Aviso 1091](#warning-1091)

[Erro fatal 1092](#fatal-error-1092)

[Erro fatal 1093](#fatal-error-1093)

[Erro fatal 1094](#fatal-error-1094)

[Erro fatal 1095](#fatal-error-1095)

[Erro fatal 1097](#fatal-error-1097)

[Erro fatal 1098](#fatal-error-1098)

[Erro fatal 1099](#fatal-error-1099)

## <a name="warning-1091"></a>Aviso 1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Aviso>: " fileName :<linha> cláusula IMPLIED não é permitida para objetos &lt; &gt; de tamanho \# fixo"**
</dt> <dd>

**Aviso semântico** de invocação de macro OBJECT-TYPE SNMPv2C específico. A palavra-chave IMPLIED só pode estar presente para um objeto que tem uma sintaxe de comprimento variável, como um OBJECT IDENTIFIER ou OCTET STRING de comprimento variável, na cláusula INDEX.

</dd> </dl>

## <a name="fatal-error-1092"></a>Erro fatal 1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: " fileName :<line> uma cláusula IMPLÍCITA não permitida para objetos potencialmente de &lt; &gt; comprimento \# zero"**
</dt> <dd>

**Erro semântico** de semântica de invocação de macro OBJECT-TYPE SNMPv2C específico. A cláusula IMPLIED não poderá ser usada em um objeto de comprimento variável se esse objeto puder ter um comprimento zero.

</dd> </dl>

## <a name="fatal-error-1093"></a>Erro fatal 1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Fatal>: " fileName<linha>: somente o tipo "INTEGER" pode ser enumerado de acordo com o &lt; &gt; \# SMI V1"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv1. Uma enumeração MIB SNMPv1 pode usar apenas o tipo INTEGER.

</dd> </dl>

## <a name="fatal-error-1094"></a>Erro fatal 1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094.> fatal: " fileName<linha>: o tipo usado na enumeração não é resolvido para um &lt; &gt; dos tipos \# permitidos"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv2C. O tipo usado em uma enumeração deve ser INTEGER ou um tipo equivalente ou outra enumeração.

</dd> </dl>

## <a name="fatal-error-1095"></a>Erro fatal 1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095.> fatal: " fileName<linha>: o membro de enumeração não é membro da &lt; &gt; \# enumeração pai"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv2C. Se outra enumeração for usada, seu conjunto de itens deverá ser um subconjunto do conjunto de itens da enumeração pai.

</dd> </dl>

## <a name="fatal-error-1097"></a>Erro fatal 1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: " fileName<line>: o nome do identificador não é resolvido para um &lt; &gt; valor \# &lt; &gt; inteiro"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv2C. Os valores no tipo BITS devem ser valores inteiros.

</dd> </dl>

## <a name="fatal-error-1098"></a>Erro fatal 1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: " &lt; fileName &gt;<line \#>: valor duplicado no &lt; &gt; constructo bits"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv2C. Não deve haver nomes e valores duplicados em um constructo BITS. O <linha> parâmetro é a \# posição da recorrência do nome/valor.

</dd> </dl>

## <a name="fatal-error-1099"></a>Erro fatal 1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: " fileName<line>: Identificador de nome duplicado no &lt; &gt; \# &lt; &gt; constructo bits"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv2C. Não deve haver nomes e valores duplicados em um constructo BITS. O <linha> parâmetro é a \# posição da recorrência do nome/valor.

</dd> </dl>

 

 



