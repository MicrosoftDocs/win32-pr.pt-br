---
description: Descreve os erros do provedor SNMP WMI 1041 a 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Erros 1041 a 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef466d1b1226b14d895fef81be24baee45354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010816"
---
# <a name="errors-1041-through-1050"></a><span data-ttu-id="6faaf-103">Erros 1041 a 1050</span><span class="sxs-lookup"><span data-stu-id="6faaf-103">Errors 1041 through 1050</span></span>

<span data-ttu-id="6faaf-104">Descreve os erros do provedor SNMP WMI 1041 a 1050.</span><span class="sxs-lookup"><span data-stu-id="6faaf-104">Describes WMI SNMP provider errors 1041 through 1050.</span></span>

[<span data-ttu-id="6faaf-105">Erro fatal 1041</span><span class="sxs-lookup"><span data-stu-id="6faaf-105">Fatal Error 1041</span></span>](#fatal-error-1041)

[<span data-ttu-id="6faaf-106">Erro fatal 1042</span><span class="sxs-lookup"><span data-stu-id="6faaf-106">Fatal Error 1042</span></span>](#fatal-error-1042)

[<span data-ttu-id="6faaf-107">Aviso 1043</span><span class="sxs-lookup"><span data-stu-id="6faaf-107">Warning 1043</span></span>](#warning-1043)

[<span data-ttu-id="6faaf-108">Erro fatal 1044</span><span class="sxs-lookup"><span data-stu-id="6faaf-108">Fatal Error 1044</span></span>](#fatal-error-1044)

[<span data-ttu-id="6faaf-109">Aviso 1045</span><span class="sxs-lookup"><span data-stu-id="6faaf-109">Warning 1045</span></span>](#warning-1045)

[<span data-ttu-id="6faaf-110">Aviso 1046</span><span class="sxs-lookup"><span data-stu-id="6faaf-110">Warning 1046</span></span>](#warning-1046)

[<span data-ttu-id="6faaf-111">Aviso 1047</span><span class="sxs-lookup"><span data-stu-id="6faaf-111">Warning 1047</span></span>](#warning-1047)

[<span data-ttu-id="6faaf-112">Aviso 1048</span><span class="sxs-lookup"><span data-stu-id="6faaf-112">Warning 1048</span></span>](#warning-1048)

[<span data-ttu-id="6faaf-113">Erro fatal 1049</span><span class="sxs-lookup"><span data-stu-id="6faaf-113">Fatal Error 1049</span></span>](#fatal-error-1049)

## <a name="fatal-error-1041"></a><span data-ttu-id="6faaf-114">Erro fatal 1041</span><span class="sxs-lookup"><span data-stu-id="6faaf-114">Fatal Error 1041</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041,> fatal: " <fileName><\# da linha>: <identifier> o identificador na especificação de intervalo não é resolvido para um valor integral"**</span><span class="sxs-lookup"><span data-stu-id="6faaf-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Fatal>: "<fileName><line\#>: Identifier <identifier> in range specification does not resolve to an integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-116">Erro semântico de módulo em especificação de intervalo ou de tamanho, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-116">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-117">O símbolo usado em uma especificação de tamanho deve ser resolvido para a cadeia de caracteres de OCTETO ou opaco.</span><span class="sxs-lookup"><span data-stu-id="6faaf-117">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="6faaf-118">Qualquer valor usado na especificação de um intervalo deve ser um inteiro.</span><span class="sxs-lookup"><span data-stu-id="6faaf-118">Any value used in specifying a range must be an integer.</span></span>

</dd> </dl>

## <a name="fatal-error-1042"></a><span data-ttu-id="6faaf-119">Erro fatal 1042</span><span class="sxs-lookup"><span data-stu-id="6faaf-119">Fatal Error 1042</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042,> fatal: " <fileName> linha de<\#>: o limite superior da especificação de intervalo é menor que o limite inferior"**</span><span class="sxs-lookup"><span data-stu-id="6faaf-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Fatal>: "<fileName><line\#>: Upper bound of range specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-121">Erro semântico de módulo em especificação de intervalo ou de tamanho, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-121">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-122">O símbolo usado em uma especificação de tamanho deve ser resolvido para a cadeia de caracteres de OCTETO ou opaco.</span><span class="sxs-lookup"><span data-stu-id="6faaf-122">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="6faaf-123">O limite inferior de uma especificação de intervalo ou tamanho não deve ser maior que o limite superior.</span><span class="sxs-lookup"><span data-stu-id="6faaf-123">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="warning-1043"></a><span data-ttu-id="6faaf-124">Aviso 1043</span><span class="sxs-lookup"><span data-stu-id="6faaf-124">Warning 1043</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, aviso>: " <fileName> : <linha \#>: tipo de objeto com a sintaxe" Sequence ", deve ter uma cláusula de acesso" não acessível "**</span><span class="sxs-lookup"><span data-stu-id="6faaf-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE", should have an ACCESS clause "not-accessible"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-126">Aviso semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="6faaf-126">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="6faaf-127">Uma tabela ou linha conceitual (sequência ou tipos de objetos de sequência, respectivamente) deve ser "não acessível".</span><span class="sxs-lookup"><span data-stu-id="6faaf-127">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="6faaf-128">Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-128">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1044"></a><span data-ttu-id="6faaf-129">Erro fatal 1044</span><span class="sxs-lookup"><span data-stu-id="6faaf-129">Fatal Error 1044</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044,> fatal: " <fileName> linha de<\#>: redefinição de símbolo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="6faaf-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Fatal>: "<fileName><line\#>: Redefinition of symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-131">Erro semântico de módulo, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-131">Module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-132">Redefinição de descritores de objeto, invocações de macro e ASN. 1 tipos causam um erro.</span><span class="sxs-lookup"><span data-stu-id="6faaf-132">Redefinition of object descriptors, macro invocations, and ASN.1 types cause an error.</span></span>

</dd> </dl>

## <a name="warning-1045"></a><span data-ttu-id="6faaf-133">Aviso 1045</span><span class="sxs-lookup"><span data-stu-id="6faaf-133">Warning 1045</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, aviso>: " <fileName><lineReference ao símbolo padrão <symbolName> assumido como sendo para a definição como em <moduleName> . Use as notações "Module. Symbol", se você quiser fazer referência à definição no módulo atual "**</span><span class="sxs-lookup"><span data-stu-id="6faaf-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Warning>: "<fileName><lineReference to standard symbol <symbolName> assumed to be for the definition as in <moduleName>. Use the "module.symbol" notations, if you want to refer to the definition in the current module"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-135">Aviso semântico de módulo, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-135">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-136">Um símbolo conhecido pelo compilador foi redefinido e está sendo referenciado.</span><span class="sxs-lookup"><span data-stu-id="6faaf-136">A symbol known to the compiler has been redefined, and is being referenced.</span></span> <span data-ttu-id="6faaf-137">O compilador assume a definição padrão do símbolo.</span><span class="sxs-lookup"><span data-stu-id="6faaf-137">The compiler assumes the standard definition of the symbol.</span></span> <span data-ttu-id="6faaf-138">Portanto, para usar uma redefinição do símbolo padrão, você deve usar a notação "Module. Symbol".</span><span class="sxs-lookup"><span data-stu-id="6faaf-138">Therefore, to use a redefinition of the standard symbol, you must use the "Module.Symbol" notation.</span></span>

</dd> </dl>

## <a name="warning-1046"></a><span data-ttu-id="6faaf-139">Aviso 1046</span><span class="sxs-lookup"><span data-stu-id="6faaf-139">Warning 1046</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046,> de aviso: " <fileName> linha de<\#>: <symbol> indefinido. Assumindo a definição padrão "**</span><span class="sxs-lookup"><span data-stu-id="6faaf-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Warning>: "<fileName><line\#>: <symbol> undefined. Assuming standard definition"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-141">Aviso semântico de módulo, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-141">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-142">Um símbolo conhecido pelo compilador não deve ser redefinido ou usado sem ser importado.</span><span class="sxs-lookup"><span data-stu-id="6faaf-142">A symbol known to the compiler must not be redefined or used without being imported.</span></span>

</dd> </dl>

## <a name="warning-1047"></a><span data-ttu-id="6faaf-143">Aviso 1047</span><span class="sxs-lookup"><span data-stu-id="6faaf-143">Warning 1047</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, aviso>: " <fileName> linha de<\#>: definição de tipo <symbol> definida mas não referenciada"**</span><span class="sxs-lookup"><span data-stu-id="6faaf-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Warning>: "<fileName><line\#>: Type definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-145">Aviso semântico de módulo, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-145">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-146">Todas as atribuições de valor e definições de tipo devem ser referenciadas em algum lugar.</span><span class="sxs-lookup"><span data-stu-id="6faaf-146">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="warning-1048"></a><span data-ttu-id="6faaf-147">Aviso 1048</span><span class="sxs-lookup"><span data-stu-id="6faaf-147">Warning 1048</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, aviso>: " <fileName> linha de<\#>: definição de valor <symbol> definida mas não referenciada"**</span><span class="sxs-lookup"><span data-stu-id="6faaf-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Warning>: "<fileName><line\#>: Value definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-149">Aviso semântico de módulo, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6faaf-149">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6faaf-150">Todas as atribuições de valor e definições de tipo devem ser referenciadas em algum lugar.</span><span class="sxs-lookup"><span data-stu-id="6faaf-150">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="fatal-error-1049"></a><span data-ttu-id="6faaf-151">Erro fatal 1049</span><span class="sxs-lookup"><span data-stu-id="6faaf-151">Fatal Error 1049</span></span>

<dl> <dt>

<span data-ttu-id="6faaf-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, fatal>: " <fileName> : <linha \#>: a cláusula defval não é permitida para o tipo de objeto com a sintaxe networkaddress"**</span><span class="sxs-lookup"><span data-stu-id="6faaf-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Fatal>: "<fileName>:<line\#>: DEFVAL clause not allowed for OBJECT-TYPE with SYNTAX NetworkAddress"**</span></span>
</dt> <dd>

<span data-ttu-id="6faaf-153">Erro semântico de módulo de chamada de macro de **tipo de objeto** específico de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="6faaf-153">**OBJECT-TYPE** macro invocation SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="6faaf-154">A cláusula DEFVAL não é permitida para um tipo de objeto cuja cláusula de sintaxe seja resolvida como NetworkAddress.</span><span class="sxs-lookup"><span data-stu-id="6faaf-154">The DEFVAL clause is not allowed for an OBJECT-TYPE whose SYNTAX clause resolves to NetworkAddress.</span></span>

</dd> </dl>

 

 



