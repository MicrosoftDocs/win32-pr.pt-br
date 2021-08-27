---
description: Descreve erros de provedor WMI SNMP de 1041 a 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Erros de 1041 a 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1a245f8e4da4556dd05a9827255ca2e7f168ab
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879859"
---
# <a name="errors-1041-through-1050"></a>Erros de 1041 a 1050

Descreve erros de provedor WMI SNMP de 1041 a 1050.

[Erro fatal 1041](#fatal-error-1041)

[Erro fatal 1042](#fatal-error-1042)

[Aviso 1043](#warning-1043)

[Erro fatal 1044](#fatal-error-1044)

[Aviso 1045](#warning-1045)

[Aviso 1046](#warning-1046)

[Aviso 1047](#warning-1047)

[Aviso 1048](#warning-1048)

[Erro fatal 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Erro fatal 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Fatal>: " &lt; fileName &gt;<line \#>: Identificador na especificação de intervalo não é resolvido para um &lt; &gt; valor integral"**
</dt> <dd>

Erro semântico do módulo na especificação de intervalo ou tamanho, específico para SNMPv1 nem SNMPv2C. O símbolo usado em uma especificação SIZE deve ser resolvido para OCTET STRING ou Opaque. Qualquer valor usado na especificação de um intervalo deve ser um inteiro.

</dd> </dl>

## <a name="fatal-error-1042"></a>Erro fatal 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Fatal>: " &lt; fileName<line>: o limite superior da especificação de intervalo é menor que o limite &gt; \# inferior"**
</dt> <dd>

Erro semântico do módulo na especificação de intervalo ou tamanho, específico para SNMPv1 nem SNMPv2C. O símbolo usado em uma especificação SIZE deve ser resolvido para OCTET STRING ou Opaque. O limite inferior de um intervalo ou especificação SIZE não deve ser maior que o limite superior.

</dd> </dl>

## <a name="warning-1043"></a>Aviso 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Aviso>: " &lt; fileName &gt; :<line \#>: OBJECT-TYPE with SYNTAX "SEQUENCE", deve ter uma cláusula ACCESS "não acessível"**
</dt> <dd>

**Aviso semântico do** módulo de invocação de macro OBJECT-TYPE. Uma tabela ou linha conceitual (tipos de objeto SEQUENCE OF ou SEQUENCE, respectivamente) deve ser "não acessível".

Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1044"></a>Erro fatal 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Fatal>: " &lt; fileName &gt;<line \#>: Redefinição do &lt; identificador de símbolo &gt; "**
</dt> <dd>

Erro semântico do módulo, específico para SNMPv1 nem SNMPv2C. A redefinição de descritores de objeto, invocações de macro e tipos ASN.1 causam um erro.

</dd> </dl>

## <a name="warning-1045"></a>Aviso 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Aviso>: " &lt; fileName &gt;<lineReference to standard symbol SymbolName assumido como para a definição como &lt; &gt; em &lt; moduleName &gt; . Use as notações "module.symbol", se você quiser se referir à definição no módulo atual"**
</dt> <dd>

Aviso semântico do módulo, específico para SNMPv1 nem SNMPv2C. Um símbolo conhecido pelo compilador foi redefinido e está sendo referenciado. O compilador assume a definição padrão do símbolo. Portanto, para usar uma redefinição do símbolo padrão, você deve usar a notação "Module.Symbol".

</dd> </dl>

## <a name="warning-1046"></a>Aviso 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Aviso>: " &lt; fileName<&gt; linha \#>: símbolo &lt; &gt; indefinido. Supondo a definição padrão"**
</dt> <dd>

Aviso semântico do módulo, específico para SNMPv1 nem SNMPv2C. Um símbolo conhecido pelo compilador não deve ser redefinido ou usado sem ser importado.

</dd> </dl>

## <a name="warning-1047"></a>Aviso 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Aviso>: " fileName<linha>: símbolo de definição de tipo definido, mas não &lt; &gt; \# &lt; &gt; referenciado"**
</dt> <dd>

Aviso semântico do módulo, específico para SNMPv1 nem SNMPv2C. Todas as atribuições de valor e definições de tipo devem ser referenciadas em algum lugar.

</dd> </dl>

## <a name="warning-1048"></a>Aviso 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Aviso>: " fileName<linha>: símbolo de definição de valor definido, mas não &lt; &gt; \# &lt; &gt; referenciado"**
</dt> <dd>

Aviso semântico do módulo, específico para SNMPv1 nem SNMPv2C. Todas as atribuições de valor e definições de tipo devem ser referenciadas em algum lugar.

</dd> </dl>

## <a name="fatal-error-1049"></a>Erro fatal 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Fatal>: " &lt; fileName :<line>: cláusula DEFVAL não permitida para &gt; \# OBJECT-TYPE com SYNTAX NetworkAddress"**
</dt> <dd>

**Erro semântico** de invocação de macro OBJECT-TYPE SNMPv1 específico do módulo. A cláusula DEFVAL não é permitida para um OBJECT-TYPE cuja cláusula SYNTAX é resolvida como NetworkAddress.

</dd> </dl>

 

 



