---
description: Descreve os erros do provedor SNMP WMI 1011 a 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Erros 1011 a 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a73f90ce0fc161604d87672fb5b33f9708aa945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011505"
---
# <a name="errors-1011-through-1020"></a><span data-ttu-id="dacbd-103">Erros 1011 a 1020</span><span class="sxs-lookup"><span data-stu-id="dacbd-103">Errors 1011 through 1020</span></span>

<span data-ttu-id="dacbd-104">Descreve os erros do provedor SNMP WMI 1011 a 1020.</span><span class="sxs-lookup"><span data-stu-id="dacbd-104">Describes WMI SNMP provider errors 1011 through 1020.</span></span>

[<span data-ttu-id="dacbd-105">Erro fatal 1011</span><span class="sxs-lookup"><span data-stu-id="dacbd-105">Fatal Error 1011</span></span>](#fatal-error-1011)

[<span data-ttu-id="dacbd-106">Erro fatal 1012</span><span class="sxs-lookup"><span data-stu-id="dacbd-106">Fatal Error 1012</span></span>](#fatal-error-1012)

[<span data-ttu-id="dacbd-107">Erro fatal 1013</span><span class="sxs-lookup"><span data-stu-id="dacbd-107">Fatal Error 1013</span></span>](#fatal-error-1013)

[<span data-ttu-id="dacbd-108">Aviso 1014</span><span class="sxs-lookup"><span data-stu-id="dacbd-108">Warning 1014</span></span>](#warning-1014)

[<span data-ttu-id="dacbd-109">Erro fatal 1015</span><span class="sxs-lookup"><span data-stu-id="dacbd-109">Fatal Error 1015</span></span>](#fatal-error-1015)

[<span data-ttu-id="dacbd-110">Erro fatal 1016</span><span class="sxs-lookup"><span data-stu-id="dacbd-110">Fatal Error 1016</span></span>](#fatal-error-1016)

[<span data-ttu-id="dacbd-111">Erro fatal 1018</span><span class="sxs-lookup"><span data-stu-id="dacbd-111">Fatal Error 1018</span></span>](#fatal-error-1018)

[<span data-ttu-id="dacbd-112">Erro fatal 1020</span><span class="sxs-lookup"><span data-stu-id="dacbd-112">Fatal Error 1020</span></span>](#fatal-error-1020)

## <a name="fatal-error-1011"></a><span data-ttu-id="dacbd-113">Erro fatal 1011</span><span class="sxs-lookup"><span data-stu-id="dacbd-113">Fatal Error 1011</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, fatal>: " <fileName> : <linha \#> sintaxe do membro <identifier> da sequência, <identifier> , diferente da cláusula Syntax do tipo Object-Type"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Fatal>: "<fileName>:<line\#> the SYNTAX of member <identifier> of SEQUENCE, <identifier>, differs from the SYNTAX clause of the OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-115">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="dacbd-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="dacbd-116">Um elemento de uma sequência deve ser o mesmo que o tipo na cláusula de sintaxe da definição de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="dacbd-116">An element of a SEQUENCE must be same as the type in the SYNTAX clause of the OBJECT-TYPE definition.</span></span> <span data-ttu-id="dacbd-117">O parâmetro de> de linha de <\# é a linha da cláusula de sintaxe da definição de tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="dacbd-117">The <line\#> parameter is the line of the SYNTAX clause of the OBJECT-TYPE definition.</span></span>

<span data-ttu-id="dacbd-118">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dacbd-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1012"></a><span data-ttu-id="dacbd-119">Erro fatal 1012</span><span class="sxs-lookup"><span data-stu-id="dacbd-119">Fatal Error 1012</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012,> fatal: " <fileName> : <linha \#> uma cláusula de índice ou de aumentos é necessária somente para tipos de objeto de sequência"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Fatal>: "<fileName>:<line\#> An INDEX or AUGMENTS clause is required only for SEQUENCE OBJECT-TYPES"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-121">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="dacbd-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="dacbd-122">Uma cláusula de índice só deve estar presente em uma definição de tipo de objeto cuja sintaxe seja resolvida para um tipo de sequência.</span><span class="sxs-lookup"><span data-stu-id="dacbd-122">An INDEX clause must only be present in an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="dacbd-123">Esse erro pode ocorrer durante a compilação de uma MIB ou do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dacbd-123">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="fatal-error-1013"></a><span data-ttu-id="dacbd-124">Erro fatal 1013</span><span class="sxs-lookup"><span data-stu-id="dacbd-124">Fatal Error 1013</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013,> fatal: " <fileName> linha de<\#>: <identifier> deve resolver para um tipo de sequência"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Fatal>: "<fileName><line\#>: <identifier> should resolve to a SEQUENCE type"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-126">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="dacbd-126">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="dacbd-127">Um tipo usado na construção "SEQUENCE OF" deve ser resolvido para um tipo de sequência.</span><span class="sxs-lookup"><span data-stu-id="dacbd-127">A type used in the "SEQUENCE OF" construct must resolve to a SEQUENCE type.</span></span>

<span data-ttu-id="dacbd-128">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dacbd-128">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1014"></a><span data-ttu-id="dacbd-129">Aviso 1014</span><span class="sxs-lookup"><span data-stu-id="dacbd-129">Warning 1014</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, aviso>: " <fileName> : <linha \#>: sub-identificador do valor 0 não recomendado em OIDs"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Warning>: "<fileName>:<line\#>: Sub-identifier of value 0 not recommended in OIDs"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-131">Aviso semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="dacbd-131">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="dacbd-132">É recomendável que nenhum objeto em uma MIB padrão da Internet use um subidentificador de zero em seu identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="dacbd-132">It is recommended that no object in an Internet Standard MIB use a sub-identifier of zero in its OBJECT IDENTIFIER.</span></span>

<span data-ttu-id="dacbd-133">Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dacbd-133">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1015"></a><span data-ttu-id="dacbd-134">Erro fatal 1015</span><span class="sxs-lookup"><span data-stu-id="dacbd-134">Fatal Error 1015</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015,> fatal: " <fileName> : <linha \#>: OBJECT-TYPEs <identifier> do módulo <identifier> e <identifier> do módulo recebem <identifier> os mesmos valores de OID"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Fatal>: "<fileName>:<line\#>: OBJECT-TYPEs <identifier> from module <identifier> and <identifier> from module <identifier> are assigned the same OID values"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-136">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="dacbd-136">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="dacbd-137">Duas invocações de **tipo de objeto** (no mesmo ou em módulos diferentes) não devem ser atribuídas ao mesmo valor de identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="dacbd-137">Two **OBJECT-TYPE** invocations (in the same or different modules) must not be assigned the same Object Identifier value.</span></span>

<span data-ttu-id="dacbd-138">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dacbd-138">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1016"></a><span data-ttu-id="dacbd-139">Erro fatal 1016</span><span class="sxs-lookup"><span data-stu-id="dacbd-139">Fatal Error 1016</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, fatal>: " <fileName> : <linha \#>: o valor na cláusula defval não corresponde ao tipo na cláusula Syntax"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Fatal>: "<fileName>:<line\#>: Value in the DEFVAL clause does not match the type in the SYNTAX clause"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-141">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="dacbd-141">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="dacbd-142">Um valor em uma cláusula DEFVAL deve ser um valor do tipo mencionado na cláusula SYNTAX.</span><span class="sxs-lookup"><span data-stu-id="dacbd-142">A value in a DEFVAL clause must be a value of the type mentioned in the SYNTAX clause.</span></span>

<span data-ttu-id="dacbd-143">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="dacbd-143">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1018"></a><span data-ttu-id="dacbd-144">Erro fatal 1018</span><span class="sxs-lookup"><span data-stu-id="dacbd-144">Fatal Error 1018</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018,> fatal: " <fileName><\# da linha>: <symbol> na cláusula Enterprise do tipo de interceptação não é resolvido para um valor de OID"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Fatal>: "<fileName><line\#>: <symbol> in ENTERPRISE clause of TRAP-TYPE does not resolve to an OID value"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-146">Invocação de macro do **tipo Trap** , erro semântico de módulo específico de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="dacbd-146">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="dacbd-147">O símbolo usado na cláusula ENTERPRISE de uma chamada de macro do **tipo Trap** deve ser resolvido para um valor de identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="dacbd-147">The symbol used in the ENTERPRISE clause of a **TRAP-TYPE** macro invocation must resolve to an Object Identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-1020"></a><span data-ttu-id="dacbd-148">Erro fatal 1020</span><span class="sxs-lookup"><span data-stu-id="dacbd-148">Fatal Error 1020</span></span>

<dl> <dt>

<span data-ttu-id="dacbd-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020,> fatal: " <fileName><da linha \#>: o valor atribuído ao tipo de interceptação não <identifier> é resolvido para um inteiro positivo"**</span><span class="sxs-lookup"><span data-stu-id="dacbd-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Fatal>: "<fileName><line\#>: Value assigned to TRAP-TYPE <identifier> does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="dacbd-150">Invocação de macro do **tipo Trap** , erro semântico de módulo específico de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="dacbd-150">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="dacbd-151">Um símbolo usado na especificação do valor de interceptação não é resolvido como um inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="dacbd-151">A symbol used in specifying the trap value does not resolve to a positive integer.</span></span>

</dd> </dl>

 

 



