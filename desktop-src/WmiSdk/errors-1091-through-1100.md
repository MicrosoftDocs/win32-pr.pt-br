---
description: Descreve os erros do provedor SNMP WMI 1091 a 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Erros 1091 a 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf582a3df41fbc7c329f5a993555a2d76145ded0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787764"
---
# <a name="errors-1091-through-1100"></a><span data-ttu-id="251a9-103">Erros 1091 a 1100</span><span class="sxs-lookup"><span data-stu-id="251a9-103">Errors 1091 through 1100</span></span>

<span data-ttu-id="251a9-104">Descreve os erros do provedor SNMP WMI 1091 a 1100.</span><span class="sxs-lookup"><span data-stu-id="251a9-104">Describes WMI SNMP provider errors 1091 through 1100.</span></span>

[<span data-ttu-id="251a9-105">Aviso 1091</span><span class="sxs-lookup"><span data-stu-id="251a9-105">Warning 1091</span></span>](#warning-1091)

[<span data-ttu-id="251a9-106">Erro fatal 1092</span><span class="sxs-lookup"><span data-stu-id="251a9-106">Fatal Error 1092</span></span>](#fatal-error-1092)

[<span data-ttu-id="251a9-107">Erro fatal 1093</span><span class="sxs-lookup"><span data-stu-id="251a9-107">Fatal Error 1093</span></span>](#fatal-error-1093)

[<span data-ttu-id="251a9-108">Erro fatal 1094</span><span class="sxs-lookup"><span data-stu-id="251a9-108">Fatal Error 1094</span></span>](#fatal-error-1094)

[<span data-ttu-id="251a9-109">Erro fatal 1095</span><span class="sxs-lookup"><span data-stu-id="251a9-109">Fatal Error 1095</span></span>](#fatal-error-1095)

[<span data-ttu-id="251a9-110">Erro fatal 1097</span><span class="sxs-lookup"><span data-stu-id="251a9-110">Fatal Error 1097</span></span>](#fatal-error-1097)

[<span data-ttu-id="251a9-111">Erro fatal 1098</span><span class="sxs-lookup"><span data-stu-id="251a9-111">Fatal Error 1098</span></span>](#fatal-error-1098)

[<span data-ttu-id="251a9-112">Erro fatal 1099</span><span class="sxs-lookup"><span data-stu-id="251a9-112">Fatal Error 1099</span></span>](#fatal-error-1099)

## <a name="warning-1091"></a><span data-ttu-id="251a9-113">Aviso 1091</span><span class="sxs-lookup"><span data-stu-id="251a9-113">Warning 1091</span></span>

<dl> <dt>

<span data-ttu-id="251a9-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, aviso>: " <fileName> : a linha de <\#> cláusula implícita não é permitida para objetos de tamanho fixo"**</span><span class="sxs-lookup"><span data-stu-id="251a9-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: "<fileName>:<line\#> IMPLIED clause is not allowed for fixed size objects"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-115">Aviso semântico de chamada de macro do **tipo de objeto de objetos** específicos de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="251a9-115">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic warning.</span></span> <span data-ttu-id="251a9-116">A palavra-chave implícita só pode estar presente para um objeto que tenha uma sintaxe de comprimento variável, como um identificador de objeto ou uma cadeia de caracteres de OCTETO de comprimento variável, na cláusula de índice.</span><span class="sxs-lookup"><span data-stu-id="251a9-116">The IMPLIED keyword can only be present for an object having a variable-length syntax, such as an OBJECT IDENTIFIER or variable-length OCTET STRING, in the INDEX clause.</span></span>

</dd> </dl>

## <a name="fatal-error-1092"></a><span data-ttu-id="251a9-117">Erro fatal 1092</span><span class="sxs-lookup"><span data-stu-id="251a9-117">Fatal Error 1092</span></span>

<dl> <dt>

<span data-ttu-id="251a9-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, fatal>: " <fileName> : linha de <\#> cláusula implícita não permitida para objetos de comprimento potencialmente zero"**</span><span class="sxs-lookup"><span data-stu-id="251a9-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: "<fileName>:<line\#> IMPLIED clause not allowed for potentially zero-length objects"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-119">Erro semântico da chamada de macro do **tipo de objeto de objetos** específicos de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="251a9-119">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="251a9-120">A cláusula implícita não poderá ser usada em um objeto de comprimento variável se esse objeto puder ter um comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="251a9-120">The IMPLIED clause cannot be used on a variable-length object if that object can have a zero length.</span></span>

</dd> </dl>

## <a name="fatal-error-1093"></a><span data-ttu-id="251a9-121">Erro fatal 1093</span><span class="sxs-lookup"><span data-stu-id="251a9-121">Fatal Error 1093</span></span>

<dl> <dt>

<span data-ttu-id="251a9-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093.> fatal: " <fileName> linha \# de<>: somente o tipo" Integer "pode ser enumerado de acordo com o SMI v1"**</span><span class="sxs-lookup"><span data-stu-id="251a9-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Fatal>: "<fileName><line\#>: Only the type "INTEGER" can be enumerated according to the V1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-123">Atribuição de tipo, erro semântico de módulo específico de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="251a9-123">Type assignment, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="251a9-124">Uma enumeração SNMPv1 MIB pode usar apenas o tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="251a9-124">An SNMPv1 MIB enumeration can use only the type INTEGER.</span></span>

</dd> </dl>

## <a name="fatal-error-1094"></a><span data-ttu-id="251a9-125">Erro fatal 1094</span><span class="sxs-lookup"><span data-stu-id="251a9-125">Fatal Error 1094</span></span>

<dl> <dt>

<span data-ttu-id="251a9-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094.> fatal: " <fileName> linha \# de<>: o tipo usado na enumeração não é resolvido para um dos tipos permitidos"**</span><span class="sxs-lookup"><span data-stu-id="251a9-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Fatal>: "<fileName><line\#>: The type used in the enumeration does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-127">Atribuição de tipo, erro semântico de módulo específico do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="251a9-127">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="251a9-128">O tipo usado em uma enumeração deve ser inteiro ou um tipo equivalente, ou outra enumeração.</span><span class="sxs-lookup"><span data-stu-id="251a9-128">The type used in an enumeration must be INTEGER or an equivalent type, or another enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1095"></a><span data-ttu-id="251a9-129">Erro fatal 1095</span><span class="sxs-lookup"><span data-stu-id="251a9-129">Fatal Error 1095</span></span>

<dl> <dt>

<span data-ttu-id="251a9-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095.> fatal: " <fileName>> de linha de<\# : o membro de enumeração não é um membro da enumeração pai"**</span><span class="sxs-lookup"><span data-stu-id="251a9-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Fatal>: "<fileName><line\#>: Enumeration member is not a member of the parent enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-131">Atribuição de tipo, erro semântico de módulo específico do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="251a9-131">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="251a9-132">Se outra Enumeração for usada, seu conjunto de itens deverá ser um subconjunto do conjunto de itens da enumeração pai.</span><span class="sxs-lookup"><span data-stu-id="251a9-132">If another enumeration is used, its set of items must be a subset of the parent enumeration's set of items.</span></span>

</dd> </dl>

## <a name="fatal-error-1097"></a><span data-ttu-id="251a9-133">Erro fatal 1097</span><span class="sxs-lookup"><span data-stu-id="251a9-133">Fatal Error 1097</span></span>

<dl> <dt>

<span data-ttu-id="251a9-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097,> fatal: " <fileName><da linha \#>: <name> o identificador não é resolvido para um valor inteiro"**</span><span class="sxs-lookup"><span data-stu-id="251a9-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: "<fileName><line\#>: identifier <name> does not resolve to an integer value"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-135">Atribuição de tipo, erro semântico de módulo específico do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="251a9-135">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="251a9-136">Os valores no tipo BITS devem ser valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="251a9-136">The values in the BITS type must be integer values.</span></span>

</dd> </dl>

## <a name="fatal-error-1098"></a><span data-ttu-id="251a9-137">Erro fatal 1098</span><span class="sxs-lookup"><span data-stu-id="251a9-137">Fatal Error 1098</span></span>

<dl> <dt>

<span data-ttu-id="251a9-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098,> fatal: " <fileName> linha de<\#>: valor duplicado <value> na construção de bits"**</span><span class="sxs-lookup"><span data-stu-id="251a9-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: "<fileName><line\#>: Duplicate value <value> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-139">Atribuição de tipo, erro semântico de módulo específico do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="251a9-139">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="251a9-140">Não deve haver nenhum nome e valor duplicados em uma construção de BITS.</span><span class="sxs-lookup"><span data-stu-id="251a9-140">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="251a9-141">O parâmetro de> de linha de <\# é a posição da recorrência do nome/valor.</span><span class="sxs-lookup"><span data-stu-id="251a9-141">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1099"></a><span data-ttu-id="251a9-142">Erro fatal 1099</span><span class="sxs-lookup"><span data-stu-id="251a9-142">Fatal Error 1099</span></span>

<dl> <dt>

<span data-ttu-id="251a9-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099,> fatal: " <fileName> linha de<\#>: nome duplicado <identifier> na construção de bits"**</span><span class="sxs-lookup"><span data-stu-id="251a9-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="251a9-144">Atribuição de tipo, erro semântico de módulo específico do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="251a9-144">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="251a9-145">Não deve haver nenhum nome e valor duplicados em uma construção de BITS.</span><span class="sxs-lookup"><span data-stu-id="251a9-145">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="251a9-146">O parâmetro de> de linha de <\# é a posição da recorrência do nome/valor.</span><span class="sxs-lookup"><span data-stu-id="251a9-146">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

 

 



