---
description: Descreve os erros do provedor SNMP WMI 1021 a 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Erros 1021 a 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754089"
---
# <a name="errors-1021-through-1030"></a><span data-ttu-id="ab70f-103">Erros 1021 a 1030</span><span class="sxs-lookup"><span data-stu-id="ab70f-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="ab70f-104">Descreve os erros do provedor SNMP WMI 1021 a 1033.</span><span class="sxs-lookup"><span data-stu-id="ab70f-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="ab70f-105">Erro fatal 1021</span><span class="sxs-lookup"><span data-stu-id="ab70f-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="ab70f-106">Erro fatal 1022</span><span class="sxs-lookup"><span data-stu-id="ab70f-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="ab70f-107">Erro fatal 1023</span><span class="sxs-lookup"><span data-stu-id="ab70f-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="ab70f-108">Erro fatal 1024</span><span class="sxs-lookup"><span data-stu-id="ab70f-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="ab70f-109">Erro fatal 1025</span><span class="sxs-lookup"><span data-stu-id="ab70f-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="ab70f-110">Erro fatal 1026</span><span class="sxs-lookup"><span data-stu-id="ab70f-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="ab70f-111">Aviso 1027</span><span class="sxs-lookup"><span data-stu-id="ab70f-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="ab70f-112">Erro fatal 1028</span><span class="sxs-lookup"><span data-stu-id="ab70f-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="ab70f-113">Erro fatal 1029</span><span class="sxs-lookup"><span data-stu-id="ab70f-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="ab70f-114">Erro fatal 1030</span><span class="sxs-lookup"><span data-stu-id="ab70f-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="ab70f-115">Erro fatal 1021</span><span class="sxs-lookup"><span data-stu-id="ab70f-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> fatal: " <fileName><da linha \#>: <identifier> o identificador na cláusula Variables do tipo de interceptação não é resolvido para um tipo de objeto escalar"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-117">Invocação de macro do **tipo Trap** , erro semântico de módulo específico de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="ab70f-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="ab70f-118">Cada item na lista de variáveis usado na cláusula VARIABLEs de uma chamada de macro de **tipo de interceptação** deve ser resolvido para o nome de uma instância de tipo de objeto escalar.</span><span class="sxs-lookup"><span data-stu-id="ab70f-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="ab70f-119">Erro fatal 1022</span><span class="sxs-lookup"><span data-stu-id="ab70f-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> fatal: " <fileName><da linha \#>: o valor não é resolvido para o tipo <type> "**</span><span class="sxs-lookup"><span data-stu-id="ab70f-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-121">Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-122">O valor no RHS de um número inteiro, **nulo**, Cadeia de caracteres de octeto ou de valor do identificador de objeto é do tipo errado.</span><span class="sxs-lookup"><span data-stu-id="ab70f-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="ab70f-123">Erro fatal 1023</span><span class="sxs-lookup"><span data-stu-id="ab70f-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> fatal: " <fileName><da linha \#>: <identifier> o identificador não é resolvido para o tipo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="ab70f-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-125">Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-126">Um símbolo (referência de valor) no RHS de um inteiro, **nulo**, Cadeia de caracteres de octeto ou atribuição de valor de identificador de objeto não é resolvido para o tipo correto.</span><span class="sxs-lookup"><span data-stu-id="ab70f-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="ab70f-127">Erro fatal 1024</span><span class="sxs-lookup"><span data-stu-id="ab70f-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> fatal: " <fileName><da linha \#>: inteiro negativo na definição do valor de OID"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-129">Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-130">Todos os valores em uma lista de componentes de OID devem ser inteiros não negativos (preferivelmente positivos).</span><span class="sxs-lookup"><span data-stu-id="ab70f-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="ab70f-131">Erro fatal 1025</span><span class="sxs-lookup"><span data-stu-id="ab70f-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> fatal: " <identifier> o identificador no valor de OID não é resolvido para um inteiro positivo"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-133">Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-134">Todos os valores em uma lista de componentes de OID devem ser inteiros não negativos (preferivelmente positivos).</span><span class="sxs-lookup"><span data-stu-id="ab70f-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="ab70f-135">Erro fatal 1026</span><span class="sxs-lookup"><span data-stu-id="ab70f-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> fatal: " <fileName><da linha \#>: o identificador <identifier> no valor de OID não é resolvido para um valor de OID nem um inteiro positivo"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-137">Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-138">O primeiro componente usado em um valor de OID deve ser resolvido para um valor OID ou um inteiro.</span><span class="sxs-lookup"><span data-stu-id="ab70f-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="ab70f-139">Aviso 1027</span><span class="sxs-lookup"><span data-stu-id="ab70f-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, aviso>: " <fileName> linha de<\#>: símbolo importado <identifier> não utilizado"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-141">Seção de importações aviso semântico do módulo, específico para não SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-142">Um aviso é emitido para cada símbolo importado não utilizado.</span><span class="sxs-lookup"><span data-stu-id="ab70f-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="ab70f-143">Erro fatal 1028</span><span class="sxs-lookup"><span data-stu-id="ab70f-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> fatal: "módulo <identifier> não importado na seção de importações"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-145">Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-146">Um nome de módulo usado para fazer referência a um símbolo deve estar presente na cláusula Imports ou ser o nome do módulo atual.</span><span class="sxs-lookup"><span data-stu-id="ab70f-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="ab70f-147">Erro fatal 1029</span><span class="sxs-lookup"><span data-stu-id="ab70f-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> fatal: " <fileName> linha de<\#>: o módulo atual <identifier> não pode ser importado"**</span><span class="sxs-lookup"><span data-stu-id="ab70f-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-149">Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-150">O nome do módulo atual também é ilustrado na lista de importações.</span><span class="sxs-lookup"><span data-stu-id="ab70f-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="ab70f-151">Erro fatal 1030</span><span class="sxs-lookup"><span data-stu-id="ab70f-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="ab70f-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> fatal: " <fileName> linha de<\#>: símbolo <identifier> não importado do módulo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="ab70f-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="ab70f-153">Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ab70f-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ab70f-154">Você usou a notação "Module. Symbol", mas o símbolo não foi importado do módulo especificado na seção Imports.</span><span class="sxs-lookup"><span data-stu-id="ab70f-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



