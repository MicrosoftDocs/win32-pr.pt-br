---
description: Descreve os erros de provedor WMI SNMP de 1081 a 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Erros de 1081 a 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1ce7b1a8c575067fe2231108e0d314af2f8dc8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879704"
---
# <a name="errors-1081-through-1090"></a>Erros de 1081 a 1090

Descreve os erros de provedor WMI SNMP de 1081 a 1090.

[Erro fatal 1081](#fatal-error-1081)

[Erro fatal 1082](#fatal-error-1082)

[Erro fatal 1084](#fatal-error-1084)

[Aviso 1085](#warning-1085)

[Aviso 1086](#warning-1086)

[Erro fatal 1087](#fatal-error-1087)

[Erro fatal 1089](#fatal-error-1089)

[Erro fatal 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Erro fatal 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Fatal>: " &lt; fileName &gt; line \#>: &lt; Identificador &gt; de &lt; &gt; símbolo não presente no identificador de módulo importado "**
</dt> <dd>

Erro semântico de módulo em referência cruzada, específico para SNMPv1 nem SNMPv2C. Um símbolo importado de um módulo não resolve nada nesse módulo. Se esse símbolo for realmente referenciado no MIB, esse erro ocorrerá.

</dd> </dl>

## <a name="fatal-error-1082"></a>Erro fatal 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Fatal>: " &lt; fileName &gt; :<line \#>: cláusula STATUS &lt; inválida &gt; "**
</dt> <dd>

**Invocação de macro OBJECT-IDENTITY,** erro semântico de módulo específico de SNMPv2C. A cláusula STATUS de uma **invocação OBJECT-IDENTITY** deve ser "atual", "preterida" ou "obsoleta".

</dd> </dl>

## <a name="fatal-error-1084"></a>Erro fatal 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Fatal>: "fileName><line>: MODULE-IDENTITY necessária após a seção IMPORTS para todos os \# módulos SNMPv2"**
</dt> <dd>

**Invocação de macro MODULE-IDENTITY,** erro semântico de módulo específico de SNMPv2C. Deve haver uma e apenas uma invocação **MODULE-IDENTITY** em um MIB SNMPv2C, imediatamente após a seção IMPORTS.

</dd> </dl>

## <a name="warning-1085"></a>Aviso 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Aviso>: " &lt; fileName<linha>: nenhum grupo encontrado &gt; no nome do módulo \# &lt; &gt; . Não foi possível fabricar MODULE-IDENTITY. A tentativa de carregar o módulo no SMIR falhará"**
</dt> <dd>

Aviso específico do SNMPv1 semântico do módulo. Esse erro será gerado se nenhum grupo de objetos for encontrado em um módulo.

</dd> </dl>

## <a name="warning-1086"></a>Aviso 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Aviso>: " &lt; fileName<linha>: nenhum grupo encontrado &gt; no nome do módulo \# &lt; &gt; "**
</dt> <dd>

Aviso específico do SNMPv1 semântico do módulo. Esse erro será gerado se nenhum grupo de objetos for encontrado em um módulo.

</dd> </dl>

## <a name="fatal-error-1087"></a>Erro fatal 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Erro>: " &lt; fileName<linha>: cláusula STATUS inválida &gt; para uma macro \# &lt; &gt; TEXTUAL-CONVENTION"**
</dt> <dd>

Atribuição de tipo, erro semântico de módulo específico de SNMPv2C. A cláusula de status de uma invocação de macro **TEXTUAL-CONVENTION** deve ser "atual", "preterida" ou "obsoleta".

</dd> </dl>

## <a name="fatal-error-1089"></a>Erro fatal 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Fatal>: " fileName :<line>: O identificador de símbolo na cláusula AUGMENTS não é resolvido para uma &lt; &gt; linha \# &lt; &gt; OBJECT-TYPE"**
</dt> <dd>

**Erro semântico** de semântica de invocação de macro OBJECT-TYPE SNMPv2C específico. Se uma cláusula AUGMENTS estiver presente, o identificador na cláusula AUGMENTS deverá ser resolvido para uma tabela OBJECT-TYPE.

</dd> </dl>

## <a name="fatal-error-1090"></a>Erro fatal 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Fatal>: " fileName :<line> clause IMPLIED é útil apenas para o &lt; &gt; último objeto \# INDEX"**
</dt> <dd>

**Erro semântico** de semântica de invocação de macro OBJECT-TYPE SNMPv2C específico. A cláusula IMPLIED só pode ser associada ao último objeto na cláusula INDEX.

</dd> </dl>

 

 



