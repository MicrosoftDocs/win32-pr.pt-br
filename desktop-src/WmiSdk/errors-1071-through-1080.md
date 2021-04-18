---
description: Descreve os erros do provedor SNMP WMI 1071 a 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Erros 1071 a 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790582"
---
# <a name="errors-1071-through-1080"></a><span data-ttu-id="6b90f-103">Erros 1071 a 1080</span><span class="sxs-lookup"><span data-stu-id="6b90f-103">Errors 1071 through 1080</span></span>

<span data-ttu-id="6b90f-104">Descreve os erros do provedor SNMP WMI 1071 a 1080.</span><span class="sxs-lookup"><span data-stu-id="6b90f-104">Describes WMI SNMP provider errors 1071 through 1080.</span></span>

[<span data-ttu-id="6b90f-105">Aviso 1071</span><span class="sxs-lookup"><span data-stu-id="6b90f-105">Warning 1071</span></span>](#warning-1071)

[<span data-ttu-id="6b90f-106">Aviso 1072</span><span class="sxs-lookup"><span data-stu-id="6b90f-106">Warning 1072</span></span>](#warning-1072)

[<span data-ttu-id="6b90f-107">Erro fatal 1074</span><span class="sxs-lookup"><span data-stu-id="6b90f-107">Fatal Error 1074</span></span>](#fatal-error-1074)

[<span data-ttu-id="6b90f-108">Erro fatal 1075</span><span class="sxs-lookup"><span data-stu-id="6b90f-108">Fatal Error 1075</span></span>](#fatal-error-1075)

[<span data-ttu-id="6b90f-109">Erro fatal 1077</span><span class="sxs-lookup"><span data-stu-id="6b90f-109">Fatal Error 1077</span></span>](#fatal-error-1077)

[<span data-ttu-id="6b90f-110">Erro fatal 1079</span><span class="sxs-lookup"><span data-stu-id="6b90f-110">Fatal Error 1079</span></span>](#fatal-error-1079)

[<span data-ttu-id="6b90f-111">Aviso 1080</span><span class="sxs-lookup"><span data-stu-id="6b90f-111">Warning 1080</span></span>](#warning-1080)

## <a name="warning-1071"></a><span data-ttu-id="6b90f-112">Aviso 1071</span><span class="sxs-lookup"><span data-stu-id="6b90f-112">Warning 1071</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, aviso>: " <fileName> linha de<\#>: símbolo <identifier> não presente no módulo importado <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="6b90f-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Warning>: "<fileName><line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-114">Aviso semântico de módulo sobre referência cruzada, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-114">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6b90f-115">Um símbolo importado de um módulo não é resolvido para nada nesse módulo.</span><span class="sxs-lookup"><span data-stu-id="6b90f-115">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="6b90f-116">Embora esse módulo seja especificado na entrada, esse aviso é exibido.</span><span class="sxs-lookup"><span data-stu-id="6b90f-116">Even though that module is specified in the input, this warning appears.</span></span>

</dd> </dl>

## <a name="warning-1072"></a><span data-ttu-id="6b90f-117">Aviso 1072</span><span class="sxs-lookup"><span data-stu-id="6b90f-117">Warning 1072</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, aviso>: " <fileName> : <linha \#> objeto-Type <name> é um descendente do tipo Object-Type <name> do módulo <name> "**</span><span class="sxs-lookup"><span data-stu-id="6b90f-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Warning>: "<fileName>:<line\#> OBJECT-TYPE <name> is a descendant of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-119">Aviso semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="6b90f-119">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="6b90f-120">Um objeto escalar não pode ter nenhum objeto descendente.</span><span class="sxs-lookup"><span data-stu-id="6b90f-120">A scalar object cannot have any descendant objects.</span></span>

<span data-ttu-id="6b90f-121">Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-121">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1074"></a><span data-ttu-id="6b90f-122">Erro fatal 1074</span><span class="sxs-lookup"><span data-stu-id="6b90f-122">Fatal Error 1074</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, fatal>: " <fileName> : \# tipo de <de linha> Sequence (linha conceitual)-Type <name> não tem uma sequência de tipo de objeto (tabela conceitual) como seu pai"**</span><span class="sxs-lookup"><span data-stu-id="6b90f-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Fatal>: "<fileName>:<line\#> SEQUENCE (Conceptual row) OBJECT-TYPE <name> does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-124">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="6b90f-124">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6b90f-125">Cada objeto de linha deve ter um objeto Table como seu pai.</span><span class="sxs-lookup"><span data-stu-id="6b90f-125">Every row object must have a table object as its parent.</span></span>

<span data-ttu-id="6b90f-126">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-126">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1075"></a><span data-ttu-id="6b90f-127">Erro fatal 1075</span><span class="sxs-lookup"><span data-stu-id="6b90f-127">Fatal Error 1075</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, fatal>: " <fileName> : <linha \#>: o tipo de objeto <name> não pode ser um filho do tipo <name> de objeto de tabela do módulo <name> , a menos que esteja na sequência do último"**</span><span class="sxs-lookup"><span data-stu-id="6b90f-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE <name> cannot be a child of table OBJECT-TYPE <name> of module <name> unless it is in the SEQUENCE of the latter"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-129">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="6b90f-129">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6b90f-130">Cada objeto de sequência deve ter exatamente os mesmos objetos que são mencionados na definição de tipo de sequência como seus filhos.</span><span class="sxs-lookup"><span data-stu-id="6b90f-130">Every SEQUENCE object must have exactly the same objects that are mentioned in the SEQUENCE type definition as its children.</span></span> <span data-ttu-id="6b90f-131">Da mesma forma, cada sequência de objeto deve ter exatamente um filho.</span><span class="sxs-lookup"><span data-stu-id="6b90f-131">Similarly, every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="6b90f-132">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-132">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1077"></a><span data-ttu-id="6b90f-133">Erro fatal 1077</span><span class="sxs-lookup"><span data-stu-id="6b90f-133">Fatal Error 1077</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, fatal>: " <fileName> : <linha \#>: a sintaxe da tabela Object-Type <name> não é a sequência da sintaxe do tipo de objeto filho <name> do módulo <name> "**</span><span class="sxs-lookup"><span data-stu-id="6b90f-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Fatal>: "<fileName>:<line\#>: The syntax of table OBJECT-TYPE <name> is not the SEQUENCE OF the syntax of the child OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-135">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="6b90f-135">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6b90f-136">A cláusula Syntax de um objeto Table deve ser a "SEQUENCE OF" da sintaxe do objeto Row.</span><span class="sxs-lookup"><span data-stu-id="6b90f-136">The syntax clause of a table object must be the "SEQUENCE OF" of the syntax of the row object.</span></span>

<span data-ttu-id="6b90f-137">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-137">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1079"></a><span data-ttu-id="6b90f-138">Erro fatal 1079</span><span class="sxs-lookup"><span data-stu-id="6b90f-138">Fatal Error 1079</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079,> fatal: "fileName>: <line \#>: Object-Type <name> é um filho extra do tipo Object-Type <name> do módulo <name> "**</span><span class="sxs-lookup"><span data-stu-id="6b90f-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Fatal>:"fileName>:<line\#>: OBJECT-TYPE <name> is an extra child of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-140">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="6b90f-140">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="6b90f-141">Cada sequência de objeto deve ter exatamente um filho.</span><span class="sxs-lookup"><span data-stu-id="6b90f-141">Every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="6b90f-142">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-142">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1080"></a><span data-ttu-id="6b90f-143">Aviso 1080</span><span class="sxs-lookup"><span data-stu-id="6b90f-143">Warning 1080</span></span>

<dl> <dt>

<span data-ttu-id="6b90f-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, aviso>: " <fileName><linha \#>: módulo MIB <moduleName> , de onde o símbolo <symbolName> é importado, não está presente na entrada"**</span><span class="sxs-lookup"><span data-stu-id="6b90f-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="6b90f-145">Aviso semântico de módulo sobre referência cruzada, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6b90f-145">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="6b90f-146">Se um dos módulos na seção Imports do módulo principal ou de um módulo subsidiária não existir, mas os símbolos desse módulo não forem referenciados, esse aviso será exibido.</span><span class="sxs-lookup"><span data-stu-id="6b90f-146">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist, but symbols from this module are not referenced, this warning appears.</span></span>

</dd> </dl>

 

 



